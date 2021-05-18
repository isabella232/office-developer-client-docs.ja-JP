---
title: IMAPIFolderSetReadFlags
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406914"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="ae16b-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="ae16b-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="ae16b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae16b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae16b-105">**1** つ以上のフォルダーのメッセージの PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグを設定またはクリアし、読み取りレポートの送信を管理します。</span><span class="sxs-lookup"><span data-stu-id="ae16b-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ae16b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae16b-106">Parameters</span></span>

<span data-ttu-id="ae16b-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="ae16b-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="ae16b-108">[in]設定またはクリアする読み取りフラグを持つメッセージまたはメッセージを識別する [ENTRYLIST](entrylist.md) 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ae16b-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="ae16b-109">_lpMsgList が_ NULL に設定されている場合、フォルダーのすべてのメッセージの読み取りフラグが設定またはクリアされます。</span><span class="sxs-lookup"><span data-stu-id="ae16b-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="ae16b-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ae16b-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="ae16b-111">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="ae16b-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="ae16b-112">_ulUIParam_ パラメーターは _、ulFlags_ パラメーター MESSAGE_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="ae16b-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="ae16b-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="ae16b-113">_lpProgress_</span></span>
  
> <span data-ttu-id="ae16b-114">[in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ae16b-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="ae16b-115">_lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI の実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="ae16b-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="ae16b-116">_lpProgress パラメーター_ は _、ulFlags_ で MESSAGE_DIALOGフラグが設定されていない限り無視されます。</span><span class="sxs-lookup"><span data-stu-id="ae16b-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="ae16b-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ae16b-117">_ulFlags_</span></span>
  
> <span data-ttu-id="ae16b-118">[in]メッセージの読み取りフラグの設定と読み取りレポートの処理を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ae16b-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="ae16b-119">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ae16b-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="ae16b-120">CLEAR_READ_FLAG: MSGFLAG_READフラグは、PR_MESSAGE_FLAGSでクリアする必要があります。また、読み取りレポートを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae16b-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="ae16b-121">CLEAR_NRN_PENDING: MSGFLAG_NRN_PENDINGフラグは、PR_MESSAGE_FLAGSでクリアする必要があります。未読レポートは送信されません。</span><span class="sxs-lookup"><span data-stu-id="ae16b-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="ae16b-122">CLEAR_RN_PENDING: MSGFLAG_RN_PENDINGのチェック ボックスをオフPR_MESSAGE_FLAGS、読み取 **り** レポートを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae16b-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="ae16b-123">GENERATE_RECEIPT_ONLY: 保留中の場合は読み取りレポートを送信する必要がありますが、このフラグの状態に変更MSGFLAG_READがあります。</span><span class="sxs-lookup"><span data-stu-id="ae16b-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="ae16b-124">MAPI_DEFERRED_ERRORS: 操作が完了する前に **、SetReadFlags** を正常に返します。</span><span class="sxs-lookup"><span data-stu-id="ae16b-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="ae16b-125">MESSAGE_DIALOG: 操作の実行中に進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="ae16b-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="ae16b-126">SUPPRESS_RECEIPT: 読み取りレポートが要求され、この呼び出しによってメッセージの状態が未読から読み取りに変更された場合は、保留中の読み取りレポートを取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae16b-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="ae16b-127">この呼び出しでメッセージの状態が変更されない場合、メッセージ ストア プロバイダーは、このフラグを無視できます。</span><span class="sxs-lookup"><span data-stu-id="ae16b-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ae16b-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae16b-128">Return values</span></span>

<span data-ttu-id="ae16b-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae16b-129">S_OK</span></span> 
  
> <span data-ttu-id="ae16b-130">指定したメッセージまたはメッセージの読み取りフラグが正常に設定またはクリアされました。</span><span class="sxs-lookup"><span data-stu-id="ae16b-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="ae16b-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="ae16b-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="ae16b-132">メッセージ ストア プロバイダーは、読み取りレポートの抑制をサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="ae16b-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="ae16b-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ae16b-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="ae16b-134">ulFlags パラメーターでは、フラグの互換性のない組み合  _わせの 1 つが設定_ されています。</span><span class="sxs-lookup"><span data-stu-id="ae16b-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="ae16b-135">SUPPRESS_RECEIPT |CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="ae16b-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="ae16b-136">SUPPRESS_RECEIPT |CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="ae16b-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="ae16b-137">CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="ae16b-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="ae16b-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="ae16b-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="ae16b-139">呼び出しは成功しましたが、すべてのメッセージが正常に処理されたというのではありません。</span><span class="sxs-lookup"><span data-stu-id="ae16b-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="ae16b-140">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="ae16b-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="ae16b-141">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="ae16b-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="ae16b-142">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="ae16b-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae16b-143">注釈</span><span class="sxs-lookup"><span data-stu-id="ae16b-143">Remarks</span></span>

<span data-ttu-id="ae16b-144">**IMAPIFolder::SetReadFlags** メソッドは、1 つ以上のフォルダーのメッセージの PR_MESSAGE_FLAGS プロパティの **MSGFLAG_READ** フラグを設定またはクリアします。</span><span class="sxs-lookup"><span data-stu-id="ae16b-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="ae16b-145">メッセージフラグMSGFLAG_READ設定すると、メッセージは読み取りとしてマークされます。これは、必ずしも意図した受信者が実際にメッセージを読み取ったとは限りません。</span><span class="sxs-lookup"><span data-stu-id="ae16b-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="ae16b-146">**SetReadFlags は、** 読み取りレポートの送信も管理します。</span><span class="sxs-lookup"><span data-stu-id="ae16b-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="ae16b-147">次の場合は、読み取りフラグを変更できません。</span><span class="sxs-lookup"><span data-stu-id="ae16b-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="ae16b-148">存在しないメッセージ。</span><span class="sxs-lookup"><span data-stu-id="ae16b-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="ae16b-149">他の場所に移動されたメッセージ。</span><span class="sxs-lookup"><span data-stu-id="ae16b-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="ae16b-150">読み取り/書き込み権限で開いているメッセージ。</span><span class="sxs-lookup"><span data-stu-id="ae16b-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="ae16b-151">現在送信されているメッセージ。</span><span class="sxs-lookup"><span data-stu-id="ae16b-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="ae16b-152">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="ae16b-152">Notes to implementers</span></span>

<span data-ttu-id="ae16b-153">読み取りレポートの送信と、読み取りレポートを抑制する要求をサポートしない場合があります。</span><span class="sxs-lookup"><span data-stu-id="ae16b-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="ae16b-154">読み取りレポートを抑制しないようにするには _、ulFlags_ パラメーター MAPI_E_NO_SUPPRESS Set で **SetReadFlags** が呼び出SUPPRESS_RECEIPTを返します。</span><span class="sxs-lookup"><span data-stu-id="ae16b-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="ae16b-155">_lpMsgList パラメーターが_ 複数のメッセージをポイントする場合は、メッセージごとに可能な限り完全に操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="ae16b-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="ae16b-156">メモリの使い切れ、ディスク領域の使い切れ、メッセージ ストアの破損など、制御できないエラーが発生しない限り、操作を途中で停止しません。</span><span class="sxs-lookup"><span data-stu-id="ae16b-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="ae16b-157">_ulFlags_ パラメーターにフラグが設定されない場合は、次の規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="ae16b-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="ae16b-158">既MSGFLAG_READ設定されている場合は、何も行いません。</span><span class="sxs-lookup"><span data-stu-id="ae16b-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="ae16b-159">このMSGFLAG_READ設定されていない場合は、すぐに設定し **、PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されている場合は、保留中の読み取りレポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="ae16b-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="ae16b-160">このフラグSUPPRESS_RECEIPT設定すると、次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="ae16b-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="ae16b-161">既MSGFLAG_READ設定されている場合は、何も行いません。</span><span class="sxs-lookup"><span data-stu-id="ae16b-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="ae16b-162">このMSGFLAG_READ設定されていない場合は、設定し、保留中の読み取りレポートを取り消します。</span><span class="sxs-lookup"><span data-stu-id="ae16b-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="ae16b-163">このフラグCLEAR_READ_FLAG設定されている場合は、各メッセージの MSGFLAG_READ プロパティの PR_MESSAGE_FLAGS フラグをクリアし、読み取りレポートを送信しない。</span><span class="sxs-lookup"><span data-stu-id="ae16b-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="ae16b-164">このフラグGENERATE_RECEIPT_ONLY設定されている場合は、保留中の読み取りレポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="ae16b-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="ae16b-165">設定または削除を行MSGFLAG_READ。</span><span class="sxs-lookup"><span data-stu-id="ae16b-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="ae16b-166">SUPPRESS_RECEIPTフラグと GENERATE_RECEIPT_ONLY フラグの両方が設定されている場合は、PR_READ_RECEIPT_REQUESTEDを FALSE に設定し、読み取りレポートを送信しない。</span><span class="sxs-lookup"><span data-stu-id="ae16b-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ae16b-167">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ae16b-167">Notes to callers</span></span>

<span data-ttu-id="ae16b-168">これらの戻り値は、次の条件下で期待してください。</span><span class="sxs-lookup"><span data-stu-id="ae16b-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="ae16b-169">**Condition**</span><span class="sxs-lookup"><span data-stu-id="ae16b-169">**Condition**</span></span>|<span data-ttu-id="ae16b-170">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="ae16b-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae16b-171">**SetReadFlags は** 、すべてのメッセージを正常に処理しました。</span><span class="sxs-lookup"><span data-stu-id="ae16b-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="ae16b-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae16b-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="ae16b-173">**SetReadFlags は** 、すべてのメッセージを正常に処理できなかった。</span><span class="sxs-lookup"><span data-stu-id="ae16b-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="ae16b-174">MAPI_W_PARTIAL_COMPLETIONまたはMAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ae16b-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="ae16b-175">**SetReadFlags** を完了できません。</span><span class="sxs-lookup"><span data-stu-id="ae16b-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="ae16b-176">エラー以外のエラー MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ae16b-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="ae16b-177">**SetReadFlags を** 完了できない場合は、作業が完了していないと想定しません。</span><span class="sxs-lookup"><span data-stu-id="ae16b-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="ae16b-178">**エラーが発生する前に、SetReadFlags** が 1 つ以上のメッセージMSGFLAG_READフラグを設定またはクリアできた可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ae16b-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ae16b-179">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ae16b-179">MFCMAPI reference</span></span>

<span data-ttu-id="ae16b-180">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae16b-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ae16b-181">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ae16b-181">**File**</span></span>|<span data-ttu-id="ae16b-182">**関数**</span><span class="sxs-lookup"><span data-stu-id="ae16b-182">**Function**</span></span>|<span data-ttu-id="ae16b-183">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ae16b-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ae16b-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ae16b-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="ae16b-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="ae16b-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="ae16b-186">MFCMAPI は **IMAPIFolder::SetReadFlags** メソッドを使用して、指定されたメッセージの読み取り状態を手動で設定します。</span><span class="sxs-lookup"><span data-stu-id="ae16b-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae16b-187">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae16b-187">See also</span></span>

- [<span data-ttu-id="ae16b-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="ae16b-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="ae16b-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="ae16b-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="ae16b-190">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ae16b-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="ae16b-191">PidTagReadReceiptRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ae16b-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="ae16b-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ae16b-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- <span data-ttu-id="ae16b-193">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ae16b-193">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>  
- [<span data-ttu-id="ae16b-194">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="ae16b-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

