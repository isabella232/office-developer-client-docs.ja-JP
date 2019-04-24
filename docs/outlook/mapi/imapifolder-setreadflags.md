---
title: imapifoldersetreadflags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350989"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="7b762-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="7b762-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="7b762-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b762-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b762-105">1つ以上のフォルダーのメッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグを設定またはクリアし、閲覧レポートの送信を管理します。</span><span class="sxs-lookup"><span data-stu-id="7b762-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7b762-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b762-106">Parameters</span></span>

<span data-ttu-id="7b762-107">_lpmsglist_</span><span class="sxs-lookup"><span data-stu-id="7b762-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="7b762-108">順番設定またはクリアする読み取りフラグがあるメッセージまたはメッセージを識別する[entrylist](entrylist.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7b762-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="7b762-109">_lpmsglist_が NULL に設定されている場合は、すべてのフォルダーのメッセージの読み取りフラグが設定またはクリアされます。</span><span class="sxs-lookup"><span data-stu-id="7b762-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="7b762-110">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="7b762-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="7b762-111">順番進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="7b762-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="7b762-112">_uluiparam_パラメーターは、 _ulflags_パラメーターで MESSAGE_DIALOG フラグが設定されていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="7b762-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="7b762-113">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="7b762-113">_lpProgress_</span></span>
  
> <span data-ttu-id="7b762-114">順番進行状況インジケーターを表示する progress オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7b762-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="7b762-115">_lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI の実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="7b762-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="7b762-116">MESSAGE_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7b762-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="7b762-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7b762-117">_ulFlags_</span></span>
  
> <span data-ttu-id="7b762-118">順番メッセージの読み取りフラグの設定と、閲覧レポートの処理を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="7b762-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="7b762-119">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7b762-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="7b762-120">CLEAR_READ_FLAG: MSGFLAG_READ フラグを**PR_MESSAGE_FLAGS**でクリアし、閲覧レポートを送信しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b762-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="7b762-121">CLEAR_NRN_PENDING: MSGFLAG_NRN_PENDING フラグを**PR_MESSAGE_FLAGS**でクリアし、未開封のレポートを送信しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b762-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="7b762-122">CLEAR_RN_PENDING: MSGFLAG_RN_PENDING フラグを**PR_MESSAGE_FLAGS**でクリアし、閲覧レポートを送信しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b762-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="7b762-123">GENERATE_RECEIPT_ONLY: 読み取りレポートは、保留中の場合は送信されますが、MSGFLAG_READ フラグの状態は変更されません。</span><span class="sxs-lookup"><span data-stu-id="7b762-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="7b762-124">MAPI_DEFERRED_ERRORS: 操作が完了する前に、 **setreadflags**が正常に返されることを許可します。</span><span class="sxs-lookup"><span data-stu-id="7b762-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="7b762-125">MESSAGE_DIALOG: 操作が進行している間、進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="7b762-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="7b762-126">SUPPRESS_RECEIPT: 読み取りレポートが要求されている場合は、保留中の読み取りレポートを取り消す必要があります。この呼び出しは、メッセージの状態を未読から読み取りに変更します。</span><span class="sxs-lookup"><span data-stu-id="7b762-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="7b762-127">この呼び出しでメッセージの状態が変更されない場合、メッセージストアプロバイダーはこのフラグを無視できます。</span><span class="sxs-lookup"><span data-stu-id="7b762-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7b762-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b762-128">Return values</span></span>

<span data-ttu-id="7b762-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b762-129">S_OK</span></span> 
  
> <span data-ttu-id="7b762-130">指定されたメッセージまたはメッセージの読み取りフラグが正常に設定またはクリアされました。</span><span class="sxs-lookup"><span data-stu-id="7b762-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="7b762-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="7b762-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="7b762-132">メッセージストアプロバイダーは、閲覧レポートの抑制をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="7b762-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="7b762-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7b762-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="7b762-134">次のいずれかの互換性のないフラグの組み合わせが_ulflags_パラメーターで設定されています。</span><span class="sxs-lookup"><span data-stu-id="7b762-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="7b762-135">SUPPRESS_RECEIPT |CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="7b762-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="7b762-136">SUPPRESS_RECEIPT |CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="7b762-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="7b762-137">CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="7b762-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="7b762-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="7b762-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="7b762-139">呼び出しは成功しましたが、すべてのメッセージが正常に処理されませんでした。</span><span class="sxs-lookup"><span data-stu-id="7b762-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="7b762-140">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="7b762-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7b762-141">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="7b762-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7b762-142">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b762-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b762-143">解説</span><span class="sxs-lookup"><span data-stu-id="7b762-143">Remarks</span></span>

<span data-ttu-id="7b762-144">**imapifolder:: setreadflags**メソッドは、1つ以上のフォルダーのメッセージの**PR_MESSAGE_FLAGS**プロパティの MSGFLAG_READ フラグを設定またはクリアします。</span><span class="sxs-lookup"><span data-stu-id="7b762-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="7b762-145">MSGFLAG_READ フラグを設定すると、メッセージは開封済みとしてマークされます。これは、意図した受信者が実際にメッセージを読んでいることを示しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="7b762-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="7b762-146">**setreadflags**は、閲覧レポートの送信も管理します。</span><span class="sxs-lookup"><span data-stu-id="7b762-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="7b762-147">次の場合は、read フラグを変更できません。</span><span class="sxs-lookup"><span data-stu-id="7b762-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="7b762-148">存在しないメッセージ。</span><span class="sxs-lookup"><span data-stu-id="7b762-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="7b762-149">他の場所に移動されたメッセージ。</span><span class="sxs-lookup"><span data-stu-id="7b762-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="7b762-150">読み取り/書き込みアクセス許可で開いているメッセージ。</span><span class="sxs-lookup"><span data-stu-id="7b762-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="7b762-151">現在送信されているメッセージ。</span><span class="sxs-lookup"><span data-stu-id="7b762-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="7b762-152">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="7b762-152">Notes to implementers</span></span>

<span data-ttu-id="7b762-153">閲覧レポートの送信と、閲覧レポートを抑制する要求をサポートしないことを決定できます。</span><span class="sxs-lookup"><span data-stu-id="7b762-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="7b762-154">読み取りレポートを抑制しないようにするには、 **setreadflags**が_ulflags_パラメーターに set SUPPRESS_RECEIPT を指定して呼び出されたときに、MAPI_E_NO_SUPPRESS を返します。</span><span class="sxs-lookup"><span data-stu-id="7b762-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="7b762-155">_lpmsglist_パラメーターが複数のメッセージをポイントしている場合は、メッセージごとに可能な限り完全に操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="7b762-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="7b762-156">メモリが不足している、ディスクの空き領域が不足している、メッセージストアが破損しているなど、操作を途中で停止しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="7b762-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="7b762-157">_ulflags_パラメーターにどのフラグも設定されていない場合は、次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="7b762-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="7b762-158">MSGFLAG_READ が既に設定されている場合は、何も実行しません。</span><span class="sxs-lookup"><span data-stu-id="7b762-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="7b762-159">MSGFLAG_READ が設定されていない場合は、直ちに設定して、 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されている場合は、保留中の読み取りレポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="7b762-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="7b762-160">SUPPRESS_RECEIPT フラグが設定されている場合は、次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="7b762-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="7b762-161">MSGFLAG_READ が既に設定されている場合は、何も実行しません。</span><span class="sxs-lookup"><span data-stu-id="7b762-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="7b762-162">MSGFLAG_READ が設定されていない場合は、設定し、保留中のすべての開封レポートを取り消します。</span><span class="sxs-lookup"><span data-stu-id="7b762-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="7b762-163">CLEAR_READ_FLAG フラグが設定されている場合は、各メッセージの**PR_MESSAGE_FLAGS**プロパティの MSGFLAG_READ フラグをオフにして、読み取りレポートを送信しないようにします。</span><span class="sxs-lookup"><span data-stu-id="7b762-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="7b762-164">GENERATE_RECEIPT_ONLY フラグが設定されている場合は、保留中のすべての読み取りレポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="7b762-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="7b762-165">MSGFLAG_READ を設定またはクリアしません。</span><span class="sxs-lookup"><span data-stu-id="7b762-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="7b762-166">SUPPRESS_RECEIPT と GENERATE_RECEIPT_ONLY の両方のフラグが設定されている場合は、 **PR_READ_RECEIPT_REQUESTED**が設定されている場合は FALSE に設定し、閲覧レポートを送信しないようにします。</span><span class="sxs-lookup"><span data-stu-id="7b762-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7b762-167">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7b762-167">Notes to callers</span></span>

<span data-ttu-id="7b762-168">これらの戻り値は、次の条件に当てはまることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="7b762-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="7b762-169">**Condition**</span><span class="sxs-lookup"><span data-stu-id="7b762-169">**Condition**</span></span>|<span data-ttu-id="7b762-170">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="7b762-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7b762-171">**setreadflags**は、すべてのメッセージを正常に処理しました。</span><span class="sxs-lookup"><span data-stu-id="7b762-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="7b762-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b762-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="7b762-173">**setreadflags**は、すべてのメッセージを正常に処理できませんでした。</span><span class="sxs-lookup"><span data-stu-id="7b762-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="7b762-174">MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7b762-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="7b762-175">**setreadflags**を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="7b762-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="7b762-176">MAPI_E_NOT_FOUND を除くすべてのエラー値</span><span class="sxs-lookup"><span data-stu-id="7b762-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="7b762-177">**setreadflags**が完了できない場合でも、作業が行われていないとは限りません。</span><span class="sxs-lookup"><span data-stu-id="7b762-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="7b762-178">**setreadflags**は、エラーが発生する前に、1つ以上のメッセージの MSGFLAG_READ フラグを設定またはクリアできた可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7b762-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7b762-179">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="7b762-179">MFCMAPI reference</span></span>

<span data-ttu-id="7b762-180">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b762-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7b762-181">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="7b762-181">**File**</span></span>|<span data-ttu-id="7b762-182">**関数**</span><span class="sxs-lookup"><span data-stu-id="7b762-182">**Function**</span></span>|<span data-ttu-id="7b762-183">**コメント**</span><span class="sxs-lookup"><span data-stu-id="7b762-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7b762-184">folderdlg</span><span class="sxs-lookup"><span data-stu-id="7b762-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="7b762-185">cfolderdlg:: OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="7b762-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="7b762-186">mfcmapi は、指定されたメッセージに対して、 **imapifolder:: setreadflags**メソッドを使用して、手動で読み取り状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="7b762-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b762-187">関連項目</span><span class="sxs-lookup"><span data-stu-id="7b762-187">See also</span></span>

- [<span data-ttu-id="7b762-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="7b762-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="7b762-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="7b762-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="7b762-190">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7b762-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="7b762-191">PidTagReadReceiptRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7b762-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="7b762-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="7b762-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- <span data-ttu-id="7b762-193">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="7b762-193">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>  
- [<span data-ttu-id="7b762-194">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="7b762-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

