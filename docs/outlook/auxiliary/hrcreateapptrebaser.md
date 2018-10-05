---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Outlook 予定表で予定を再配置で使用する IOlkApptRebaser オブジェクトを初期化します。
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397542"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="5bae6-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="5bae6-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="5bae6-104">Outlook 予定表で予定を再配置で使用する[IOlkApptRebaser](iolkapptrebaser.md)オブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="5bae6-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5bae6-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="5bae6-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5bae6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5bae6-106">Header file:</span></span>  <br/> |<span data-ttu-id="5bae6-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="5bae6-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="5bae6-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="5bae6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5bae6-109">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="5bae6-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="5bae6-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5bae6-110">Called by:</span></span>  <br/> |<span data-ttu-id="5bae6-111">MAPI クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5bae6-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="5bae6-112">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="5bae6-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="5bae6-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="5bae6-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="5bae6-114">DLL エントリ ポイント:</span><span class="sxs-lookup"><span data-stu-id="5bae6-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="5bae6-115">**HrCreateApptRebaser@44**</span><span class="sxs-lookup"><span data-stu-id="5bae6-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="5bae6-116">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="5bae6-116">Parameters</span></span>

<span data-ttu-id="5bae6-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5bae6-117">_ulFlags_</span></span>
  
> <span data-ttu-id="5bae6-118">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bae6-118">[in] Required.</span></span> <span data-ttu-id="5bae6-119">再配置の実行方法を制御するためのフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5bae6-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="5bae6-120">次のフラグが設定でき、tzmovelib.h で定義されています。</span><span class="sxs-lookup"><span data-stu-id="5bae6-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="5bae6-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** -ユーザーは、会議の開催者の予定表アイテムが再配置されます。</span><span class="sxs-lookup"><span data-stu-id="5bae6-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="5bae6-122">既定では、こうすると、再配置されているすべての会議のすべての出席者に会議の更新を送信する Outlook に注意してください。</span><span class="sxs-lookup"><span data-stu-id="5bae6-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="5bae6-123">**REBASE_FLAG_FORCE_NO_EX_UPDATES**または**REBASE_FLAG_FORCE_NO_UPDATES**のいずれかが会議の更新の処理方法を変更するのには、このフラグを組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="5bae6-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="5bae6-124">**REBASE_FLAG_UPDATE_UNMARKED** -タイム ゾーンに設定されていない予定表アイテムを更新します。</span><span class="sxs-lookup"><span data-stu-id="5bae6-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="5bae6-125">このフラグを指定する場合にアイテムが作成されるタイム ゾーンとタイム ゾーン データがないすべてのアイテムの*pTZMissing*値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5bae6-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="5bae6-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** -唯一の定期的な予定アイテムを更新します。</span><span class="sxs-lookup"><span data-stu-id="5bae6-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="5bae6-127">**REBASE_FLAG_NO_UI** -ログオン ダイアログ ボックスのメッセージ ストアを開くときに一般に表示されるなど、ユーザー インターフェイス (UI) を表示しません。</span><span class="sxs-lookup"><span data-stu-id="5bae6-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="5bae6-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** -過去の予定表アイテムが再配置されません。</span><span class="sxs-lookup"><span data-stu-id="5bae6-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="5bae6-129">**REBASE_FLAG_FORCE_REBASE** -上の決定を再配置するための開催者を確認しないが、ユーザーは、出席者の予定表アイテムを再配置します。</span><span class="sxs-lookup"><span data-stu-id="5bae6-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="5bae6-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** -ユーザーが開催者であり、受信者が、Exchange Server に接続されていない場合にのみ更新を送信します。</span><span class="sxs-lookup"><span data-stu-id="5bae6-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="5bae6-131">**REBASE_FLAG_FORCE_NO_UPDATES** : 更新プログラムを送信することはありません。</span><span class="sxs-lookup"><span data-stu-id="5bae6-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="5bae6-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** -修正プログラムを適用する前に作成された単独の予定アイテムのみを再配置します。</span><span class="sxs-lookup"><span data-stu-id="5bae6-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="5bae6-133">**REBASE_FLAG_REPORTING_MODE** -再実際には、単なるレポートの予定アイテムを再配置されます。</span><span class="sxs-lookup"><span data-stu-id="5bae6-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="5bae6-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** -リソースに会議の更新を送信します。</span><span class="sxs-lookup"><span data-stu-id="5bae6-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="5bae6-135">_pSession_</span><span class="sxs-lookup"><span data-stu-id="5bae6-135">_pSession_</span></span>
  
> <span data-ttu-id="5bae6-136">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bae6-136">[in] Required.</span></span> <span data-ttu-id="5bae6-137">MAPI セッションのインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5bae6-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="5bae6-138">_pCalendarMsgStore_</span><span class="sxs-lookup"><span data-stu-id="5bae6-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="5bae6-139">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bae6-139">[in] Required.</span></span> <span data-ttu-id="5bae6-140">再配置する予定のアイテムを含むメッセージ ストアへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5bae6-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="5bae6-141">_pCalendarFolder_</span><span class="sxs-lookup"><span data-stu-id="5bae6-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="5bae6-142">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bae6-142">[in] Required.</span></span> <span data-ttu-id="5bae6-143">再配置する予定のアイテムが含まれている予定表フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5bae6-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="5bae6-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="5bae6-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="5bae6-145">[in]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="5bae6-145">[in] Optional.</span></span> <span data-ttu-id="5bae6-146">会議出席依頼の前に付加するプレフィックスを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5bae6-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="5bae6-147">NULL である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5bae6-147">May be NULL.</span></span>
    
<span data-ttu-id="5bae6-148">_pftInstallDateUTC_</span><span class="sxs-lookup"><span data-stu-id="5bae6-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="5bae6-149">[in]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="5bae6-149">[in] Optional.</span></span> <span data-ttu-id="5bae6-150">タイム ゾーン更新プログラムでは、日付をインストールします。</span><span class="sxs-lookup"><span data-stu-id="5bae6-150">The time zone patch install date.</span></span> <span data-ttu-id="5bae6-151">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH**フラグが設定されている場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="5bae6-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="5bae6-152">_IExpansionDepth_</span><span class="sxs-lookup"><span data-stu-id="5bae6-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="5bae6-153">[in]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="5bae6-153">[in] Optional.</span></span> <span data-ttu-id="5bae6-154">配布を展開する Exchange Server に接続されている受信者を除外する一覧に表示するときの拡張の深さです。</span><span class="sxs-lookup"><span data-stu-id="5bae6-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="5bae6-155">**REBASE_FLAG_FORCE_NO_EX_UPDATES**フラグが設定されている場合にのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="5bae6-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="5bae6-156">_pTZTo_</span><span class="sxs-lookup"><span data-stu-id="5bae6-156">_pTZTo_</span></span>
  
> <span data-ttu-id="5bae6-157">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bae6-157">[in] Required.</span></span> <span data-ttu-id="5bae6-158">再配置するタイム ゾーンを記述する**TZDEFINITION**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5bae6-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="5bae6-159">**TZDEFINITION**は、tzmovelib で定義されます。</span><span class="sxs-lookup"><span data-stu-id="5bae6-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="5bae6-160">pTZMissing</span><span class="sxs-lookup"><span data-stu-id="5bae6-160">pTZMissing</span></span>
  
> <span data-ttu-id="5bae6-161">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bae6-161">[in] Required.</span></span> <span data-ttu-id="5bae6-162">アイテムにタイム ゾーン情報がスタンプされていないかどうかを前提とするタイム ゾーンを記述する**TZDEFINITION**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5bae6-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="5bae6-163">できませんが NULL の場合、 **REBASE_FLAG_UPDATE_UNMARKED**フラグが設定されている場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="5bae6-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="5bae6-164">_ppError_</span><span class="sxs-lookup"><span data-stu-id="5bae6-164">_ppError_</span></span>
  
> <span data-ttu-id="5bae6-165">[out]エラーのバージョン、コンポーネント、およびコンテキストの情報を保持する**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5bae6-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="5bae6-166">拡張エラー情報が必要ない場合、NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5bae6-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="5bae6-167">[MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx)を解放します。</span><span class="sxs-lookup"><span data-stu-id="5bae6-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="5bae6-168">_ppApptRebase_</span><span class="sxs-lookup"><span data-stu-id="5bae6-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="5bae6-169">[out]返される**IOlkApptRebaser**インターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5bae6-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="5bae6-170">戻り値</span><span class="sxs-lookup"><span data-stu-id="5bae6-170">Return values</span></span>

<span data-ttu-id="5bae6-171">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="5bae6-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5bae6-172">解釈</span><span class="sxs-lookup"><span data-stu-id="5bae6-172">Remarks</span></span>

<span data-ttu-id="5bae6-173">[GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx)を使用して、tzmovelib.dll では、この関数のアドレスを検索するのには、プロシージャ名として**HrCreateApptRebaser@44**を指定します。</span><span class="sxs-lookup"><span data-stu-id="5bae6-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="5bae6-174">すべてのフラグは、相互の組み合わせで有効です。</span><span class="sxs-lookup"><span data-stu-id="5bae6-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="5bae6-175">さまざまなオプションの詳細についてを参照してください「Outlook タイム ゾーン データ更新ツールのコマンド ライン オプションの用語集」で[KB 931667: Microsoft Office Outlook 用タイム ゾーン データ更新ツールを使用してアドレスのタイム ゾーンの変更方法](https://support.microsoft.com/kb/931667/en-us)。</span><span class="sxs-lookup"><span data-stu-id="5bae6-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5bae6-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="5bae6-176">See also</span></span>

- [<span data-ttu-id="5bae6-177">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="5bae6-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

