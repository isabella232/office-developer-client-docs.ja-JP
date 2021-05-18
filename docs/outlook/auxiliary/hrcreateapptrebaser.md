---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: IOlkApptRebaser オブジェクトを初期化して、予定表の予定を再Outlookします。
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317613"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="5a1dd-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="5a1dd-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="5a1dd-104">[IOlkApptRebaser](iolkapptrebaser.md)オブジェクトを初期化して、予定表の予定を再Outlookします。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5a1dd-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="5a1dd-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a1dd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5a1dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="5a1dd-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="5a1dd-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="5a1dd-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="5a1dd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5a1dd-109">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="5a1dd-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="5a1dd-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5a1dd-110">Called by:</span></span>  <br/> |<span data-ttu-id="5a1dd-111">MAPI クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5a1dd-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="5a1dd-112">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="5a1dd-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="5a1dd-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="5a1dd-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="5a1dd-114">DLL エントリ ポイント:</span><span class="sxs-lookup"><span data-stu-id="5a1dd-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="5a1dd-115">**HrCreateApptRebaser@44**</span><span class="sxs-lookup"><span data-stu-id="5a1dd-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a><span data-ttu-id="5a1dd-116">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5a1dd-116">Parameters</span></span>

<span data-ttu-id="5a1dd-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5a1dd-117">_ulFlags_</span></span>
  
> <span data-ttu-id="5a1dd-118">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-118">[in] Required.</span></span> <span data-ttu-id="5a1dd-119">再調整の実行方法を制御するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="5a1dd-120">次のフラグを設定し、tzmovelib.h で定義できます。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="5a1dd-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —ユーザーが会議開催者である予定アイテムが再ベースされます。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="5a1dd-122">既定では、会議の更新Outlook、再ベースされている会議のすべての出席者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="5a1dd-123">このフラグを会議の更新プログラムまたは **REBASE_FLAG_FORCE_NO_EX_UPDATESまたはREBASE_FLAG_FORCE_NO_UPDATES** して、 **会議の更新** の処理方法を変更できます。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="5a1dd-124">**REBASE_FLAG_UPDATE_UNMARKED** — タイム ゾーンでマークされていない予定アイテムを更新します。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="5a1dd-125">このフラグを指定すると  *、pTZMissing*  値は、タイム ゾーン データを持つすべてのアイテムに対してアイテムが作成されるタイム ゾーンとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="5a1dd-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —定期的な予定アイテムのみを更新します。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="5a1dd-127">**REBASE_FLAG_NO_UI** —メッセージ ストアを開く際に一般的に表示されるログオン ダイアログ ボックスを含む、ユーザー インターフェイス (UI) を表示しない。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="5a1dd-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —過去に発生した予定アイテムを再ベースにしません。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="5a1dd-129">**REBASE_FLAG_FORCE_REBASE** —開催者に決定の再送信を確認しないが、ユーザーが出席者である予定アイテムを再ベース化します。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="5a1dd-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —ユーザーがオーガナイザーであり、受信者がユーザーに接続されていない場合にのみ更新プログラムを送信Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="5a1dd-131">**REBASE_FLAG_FORCE_NO_UPDATES** —更新プログラムを送信しない。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="5a1dd-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —更新プログラムが適用される前に作成された単一インスタンスの予定アイテムのみをリベースします。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="5a1dd-133">**REBASE_FLAG_REPORTING_MODE** —実際にはリベースを行うのではなく、リベースされる予定アイテムを報告してください。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="5a1dd-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —会議の更新プログラムをリソースに送信します。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="5a1dd-135">_pSession_</span><span class="sxs-lookup"><span data-stu-id="5a1dd-135">_pSession_</span></span>
  
> <span data-ttu-id="5a1dd-136">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-136">[in] Required.</span></span> <span data-ttu-id="5a1dd-137">MAPI セッション インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="5a1dd-138">_pCalendarMsgStore_</span><span class="sxs-lookup"><span data-stu-id="5a1dd-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="5a1dd-139">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-139">[in] Required.</span></span> <span data-ttu-id="5a1dd-140">リベースする予定アイテムを含むメッセージ ストアへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="5a1dd-141">_pCalendarFolder_</span><span class="sxs-lookup"><span data-stu-id="5a1dd-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="5a1dd-142">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-142">[in] Required.</span></span> <span data-ttu-id="5a1dd-143">再ベースする予定アイテムを含む予定表フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="5a1dd-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="5a1dd-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="5a1dd-145">[in]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-145">[in] Optional.</span></span> <span data-ttu-id="5a1dd-146">会議出席依頼の先頭に付加されるプレフィックスを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="5a1dd-147">NULL の場合があります。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-147">May be NULL.</span></span>
    
<span data-ttu-id="5a1dd-148">_pftInstallDateUTC_</span><span class="sxs-lookup"><span data-stu-id="5a1dd-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="5a1dd-149">[in]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-149">[in] Optional.</span></span> <span data-ttu-id="5a1dd-150">タイム ゾーンパッチのインストール日。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-150">The time zone patch install date.</span></span> <span data-ttu-id="5a1dd-151">このフラグ **がREBASE_FLAG_ONLY_CREATED_PRE_PATCH場合** にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="5a1dd-152">_IExpansionDepth_</span><span class="sxs-lookup"><span data-stu-id="5a1dd-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="5a1dd-153">[in]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-153">[in] Optional.</span></span> <span data-ttu-id="5a1dd-154">配布リストを展開して、配布リストに接続されている受信者を除外する場合の拡張Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="5a1dd-155">このフラグが設定されている **REBASE_FLAG_FORCE_NO_EX_UPDATES** のみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="5a1dd-156">_pTZTo_</span><span class="sxs-lookup"><span data-stu-id="5a1dd-156">_pTZTo_</span></span>
  
> <span data-ttu-id="5a1dd-157">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-157">[in] Required.</span></span> <span data-ttu-id="5a1dd-158">再ベースするタイム ゾーンを記述する **TZDEFINITION** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="5a1dd-159">**TZDEFINITION は** tzmovelib で定義されます。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="5a1dd-160">pTZMissing</span><span class="sxs-lookup"><span data-stu-id="5a1dd-160">pTZMissing</span></span>
  
> <span data-ttu-id="5a1dd-161">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-161">[in] Required.</span></span> <span data-ttu-id="5a1dd-162">タイム ゾーン情報がアイテムにスタンプされていない場合に想定されるタイム ゾーンを記述する **TZDEFINITION** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="5a1dd-163">NULL にすることはできませんが、このフラグが設定されている **REBASE_FLAG_UPDATE_UNMARKED使用してください** 。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="5a1dd-164">_ppError_</span><span class="sxs-lookup"><span data-stu-id="5a1dd-164">_ppError_</span></span>
  
> <span data-ttu-id="5a1dd-165">[out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="5a1dd-166">拡張エラー情報が必要ない場合は NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="5a1dd-167">[MAPIFreeBuffer で無料](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx)です。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="5a1dd-168">_ppApptRebase_</span><span class="sxs-lookup"><span data-stu-id="5a1dd-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="5a1dd-169">[out]返される **IOlkApptRebaser インターフェイスへのポインターを指すポインター** 。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="5a1dd-170">戻り値</span><span class="sxs-lookup"><span data-stu-id="5a1dd-170">Return values</span></span>

<span data-ttu-id="5a1dd-171">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a1dd-172">注釈</span><span class="sxs-lookup"><span data-stu-id="5a1dd-172">Remarks</span></span>

<span data-ttu-id="5a1dd-173">[GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx)を使用してこの関数のアドレスを検索する場合は **tzmovelib.dllプロシージャHrCreateApptRebaser@44** として指定します。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="5a1dd-174">すべてのフラグが互いに組み合わせて有効な場合ではありません。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="5a1dd-175">さまざまなオプションの詳細については、KB [931667](https://support.microsoft.com/kb/931667/en-us)の「Outlook タイム ゾーン データ更新ツールのコマンド ライン オプションの用語集」を参照してください。Microsoft Office Outlook のタイム ゾーン データ更新ツールを使用してタイム ゾーンの変更に対処する方法。</span><span class="sxs-lookup"><span data-stu-id="5a1dd-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5a1dd-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a1dd-176">See also</span></span>

- [<span data-ttu-id="5a1dd-177">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="5a1dd-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

