---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Outlook の予定表で予定を再配置するときに使用する IOlkApptRebaser オブジェクトを初期化します。
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317613"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="8839c-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="8839c-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="8839c-104">Outlook の予定表で予定を再配置するときに使用する[IOlkApptRebaser](iolkapptrebaser.md)オブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8839c-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8839c-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="8839c-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8839c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8839c-106">Header file:</span></span>  <br/> |<span data-ttu-id="8839c-107">、tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="8839c-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="8839c-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="8839c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8839c-109">、tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="8839c-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="8839c-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="8839c-110">Called by:</span></span>  <br/> |<span data-ttu-id="8839c-111">MAPI クライアントアプリケーション</span><span class="sxs-lookup"><span data-stu-id="8839c-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="8839c-112">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="8839c-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="8839c-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="8839c-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="8839c-114">DLL エントリポイント:</span><span class="sxs-lookup"><span data-stu-id="8839c-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="8839c-115">**hrcreateapptrebaser @ 44**</span><span class="sxs-lookup"><span data-stu-id="8839c-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="8839c-116">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8839c-116">Parameters</span></span>

<span data-ttu-id="8839c-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8839c-117">_ulFlags_</span></span>
  
> <span data-ttu-id="8839c-118">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="8839c-118">[in] Required.</span></span> <span data-ttu-id="8839c-119">リベースの実行方法を制御するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8839c-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="8839c-120">、tzmovelib.h では、次のフラグを設定および定義できます。</span><span class="sxs-lookup"><span data-stu-id="8839c-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="8839c-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —ユーザーが会議の開催者になっている予定アイテムが再配置されます。</span><span class="sxs-lookup"><span data-stu-id="8839c-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="8839c-122">既定では、この設定により、再配置されているすべての会議の出席者全員に会議の更新が送信されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8839c-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="8839c-123">このフラグを**REBASE_FLAG_FORCE_NO_EX_UPDATES**または**REBASE_FLAG_FORCE_NO_UPDATES**と組み合わせて、会議の更新の処理方法を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="8839c-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="8839c-124">**REBASE_FLAG_UPDATE_UNMARKED** —タイムゾーンが設定されていない予定アイテムを更新します。</span><span class="sxs-lookup"><span data-stu-id="8839c-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="8839c-125">このフラグが指定されている場合は、タイムゾーンデータを持たないすべてのアイテムに対してアイテムが作成されるタイムゾーンとして、 *ptzmissing*の値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="8839c-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="8839c-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** -定期的な予定アイテムのみを更新します。</span><span class="sxs-lookup"><span data-stu-id="8839c-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="8839c-127">**REBASE_FLAG_NO_UI** —メッセージストアを開くときに通常表示されるログオンダイアログボックスなど、ユーザーインターフェイス (UI) を表示しません。</span><span class="sxs-lookup"><span data-stu-id="8839c-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="8839c-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** -過去に発生した予定アイテムを再配置しません。</span><span class="sxs-lookup"><span data-stu-id="8839c-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="8839c-129">**REBASE_FLAG_FORCE_REBASE** —開催者による再配置の決定をチェックせず、ユーザーが出席者になっている予定アイテムを再配置します。</span><span class="sxs-lookup"><span data-stu-id="8839c-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="8839c-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —ユーザーが開催者であり、受信者が Exchange サーバーに接続されていない場合にのみ、更新を送信します。</span><span class="sxs-lookup"><span data-stu-id="8839c-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="8839c-131">**REBASE_FLAG_FORCE_NO_UPDATES** -更新を送信しません。</span><span class="sxs-lookup"><span data-stu-id="8839c-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="8839c-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** -パッチを適用する前に作成された単一インスタンスの予定アイテムのみをリベースします。</span><span class="sxs-lookup"><span data-stu-id="8839c-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="8839c-133">**REBASE_FLAG_REPORTING_MODE** -再配置される予定アイテムを報告するだけで、実際には再配置しないようにします。</span><span class="sxs-lookup"><span data-stu-id="8839c-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="8839c-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —リソースに会議の更新を送信します。</span><span class="sxs-lookup"><span data-stu-id="8839c-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="8839c-135">_psession_</span><span class="sxs-lookup"><span data-stu-id="8839c-135">_pSession_</span></span>
  
> <span data-ttu-id="8839c-136">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="8839c-136">[in] Required.</span></span> <span data-ttu-id="8839c-137">MAPI セッションインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8839c-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="8839c-138">_pcalendarmsgstore_</span><span class="sxs-lookup"><span data-stu-id="8839c-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="8839c-139">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="8839c-139">[in] Required.</span></span> <span data-ttu-id="8839c-140">再配置する予定アイテムを含むメッセージストアへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8839c-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="8839c-141">_pcalendarfolder_</span><span class="sxs-lookup"><span data-stu-id="8839c-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="8839c-142">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="8839c-142">[in] Required.</span></span> <span data-ttu-id="8839c-143">再配置する予定アイテムを含む予定表フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8839c-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="8839c-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="8839c-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="8839c-145">[in]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="8839c-145">[in] Optional.</span></span> <span data-ttu-id="8839c-146">会議出席依頼の先頭に付加するプレフィックスを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8839c-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="8839c-147">NULL の場合があります。</span><span class="sxs-lookup"><span data-stu-id="8839c-147">May be NULL.</span></span>
    
<span data-ttu-id="8839c-148">_pftinstalldateutc_</span><span class="sxs-lookup"><span data-stu-id="8839c-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="8839c-149">[in]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="8839c-149">[in] Optional.</span></span> <span data-ttu-id="8839c-150">タイムゾーンパッチのインストールの日付。</span><span class="sxs-lookup"><span data-stu-id="8839c-150">The time zone patch install date.</span></span> <span data-ttu-id="8839c-151">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH**フラグが設定されている場合にのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="8839c-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="8839c-152">_i の色_</span><span class="sxs-lookup"><span data-stu-id="8839c-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="8839c-153">[in]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="8839c-153">[in] Optional.</span></span> <span data-ttu-id="8839c-154">Exchange Server に接続されている受信者を除外するために配布リストを展開するときの拡張の深さ。</span><span class="sxs-lookup"><span data-stu-id="8839c-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="8839c-155">**REBASE_FLAG_FORCE_NO_EX_UPDATES**フラグが設定されている場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="8839c-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="8839c-156">_ptzto_</span><span class="sxs-lookup"><span data-stu-id="8839c-156">_pTZTo_</span></span>
  
> <span data-ttu-id="8839c-157">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="8839c-157">[in] Required.</span></span> <span data-ttu-id="8839c-158">再配置するタイムゾーンを記述する**TZDEFINITION**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8839c-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="8839c-159">**TZDEFINITION**は、、tzmovelib.h で定義されています。</span><span class="sxs-lookup"><span data-stu-id="8839c-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="8839c-160">ptzmissing</span><span class="sxs-lookup"><span data-stu-id="8839c-160">pTZMissing</span></span>
  
> <span data-ttu-id="8839c-161">[in]必要があります。</span><span class="sxs-lookup"><span data-stu-id="8839c-161">[in] Required.</span></span> <span data-ttu-id="8839c-162">タイムゾーン情報がアイテムにスタンプされていない場合に想定されるタイムゾーンを説明する**TZDEFINITION**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8839c-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="8839c-163">NULL にすることはできませんが、 **REBASE_FLAG_UPDATE_UNMARKED**フラグが設定されている場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="8839c-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="8839c-164">_pperror_</span><span class="sxs-lookup"><span data-stu-id="8839c-164">_ppError_</span></span>
  
> <span data-ttu-id="8839c-165">読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8839c-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="8839c-166">拡張エラー情報を必要としない場合は、NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="8839c-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="8839c-167">[MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx)を使用して無料で使用できます。</span><span class="sxs-lookup"><span data-stu-id="8839c-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="8839c-168">_ppapptrebase_</span><span class="sxs-lookup"><span data-stu-id="8839c-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="8839c-169">読み上げ返された**IOlkApptRebaser**インターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8839c-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8839c-170">戻り値</span><span class="sxs-lookup"><span data-stu-id="8839c-170">Return values</span></span>

<span data-ttu-id="8839c-171">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="8839c-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8839c-172">解説</span><span class="sxs-lookup"><span data-stu-id="8839c-172">Remarks</span></span>

<span data-ttu-id="8839c-173">[GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx)を使用して、tzmovelib.h でこの関数のアドレスを検索する場合は、プロシージャ名として**hrcreateapptrebaser @ 44**を指定します。</span><span class="sxs-lookup"><span data-stu-id="8839c-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="8839c-174">すべてのフラグが互いに組み合わせて有効なわけではありません。</span><span class="sxs-lookup"><span data-stu-id="8839c-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="8839c-175">さまざまなオプションの詳細については、「 [KB 931667: time zone data update tool for Microsoft Office Outlook を使用してタイムゾーンの変更に対処する方法](https://support.microsoft.com/kb/931667/en-us)」の「Outlook タイムゾーンデータ更新ツールのコマンドラインオプションの用語集」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8839c-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8839c-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="8839c-176">See also</span></span>

- [<span data-ttu-id="8839c-177">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="8839c-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

