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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 88185efea344844016547d0844277de6e0d661db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578319"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="5972b-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="5972b-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="5972b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5972b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5972b-105">設定または、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティに 1 つまたは複数のフォルダーのメッセージでは、MSGFLAG_READ フラグをクリアし、リードのレポートの送信を管理します。</span><span class="sxs-lookup"><span data-stu-id="5972b-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5972b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5972b-106">Parameters</span></span>

<span data-ttu-id="5972b-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="5972b-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="5972b-108">[in]メッセージのフラグをオンまたはオフに読み取られたメッセージを識別する[ENTRYLIST](entrylist.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5972b-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="5972b-109">_LpMsgList_は、NULL に設定されている場合、読み取りはすべてフォルダーのメッセージを設定またはクリアのフラグです。</span><span class="sxs-lookup"><span data-stu-id="5972b-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="5972b-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5972b-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="5972b-111">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="5972b-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="5972b-112">_UlFlags_パラメーターに MESSAGE_DIALOG フラグが設定されていない限り、 _ulUIParam_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="5972b-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="5972b-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="5972b-113">_lpProgress_</span></span>
  
> <span data-ttu-id="5972b-114">[in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5972b-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="5972b-115">_LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI の実装を使用して進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="5972b-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="5972b-116">_UlFlags_に MESSAGE_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="5972b-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="5972b-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5972b-117">_ulFlags_</span></span>
  
> <span data-ttu-id="5972b-118">[in]メッセージの読み取りフラグの設定の処理を制御するフラグのビットマスクは、レポートをお読みください。</span><span class="sxs-lookup"><span data-stu-id="5972b-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="5972b-119">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5972b-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="5972b-120">CLEAR_READ_FLAG: **PR_MESSAGE_FLAGS**に MSGFLAG_READ フラグをクリアする必要があり、リードのレポートは送信されませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5972b-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="5972b-121">CLEAR_NRN_PENDING: **PR_MESSAGE_FLAGS**に MSGFLAG_NRN_PENDING フラグをクリアする必要があり、未読のレポートを送信しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="5972b-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="5972b-122">CLEAR_RN_PENDING: **PR_MESSAGE_FLAGS**に MSGFLAG_RN_PENDING フラグをクリアする必要があり、リードのレポートは送信されませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5972b-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="5972b-123">GENERATE_RECEIPT_ONLY: 1 つは、保留中が存在しないはずの MSGFLAG_READ フラグの状態の変更は、リードのレポートを送信してください。</span><span class="sxs-lookup"><span data-stu-id="5972b-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="5972b-124">MAPI_DEFERRED_ERRORS: 正常に完了可能性がありますが、操作を完了する前にするには**SetReadFlags**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="5972b-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="5972b-125">MESSAGE_DIALOG: は、操作の進行中に進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="5972b-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="5972b-126">SUPPRESS_RECEIPT: 要求された読み取りのレポートと、この呼び出しからの読み取りに未読のメッセージの状態を変更する場合は、保留中の読み取りレポートをキャンセルするか。</span><span class="sxs-lookup"><span data-stu-id="5972b-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="5972b-127">この呼び出しで、メッセージの状態が変化しない場合、メッセージ ストア プロバイダーは、このフラグを無視できます。</span><span class="sxs-lookup"><span data-stu-id="5972b-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="5972b-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="5972b-128">Return values</span></span>

<span data-ttu-id="5972b-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="5972b-129">S_OK</span></span> 
  
> <span data-ttu-id="5972b-130">読み取り、指定したメッセージまたはメッセージのフラグを設定またはクリアに成功しました。</span><span class="sxs-lookup"><span data-stu-id="5972b-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="5972b-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="5972b-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="5972b-132">メッセージ ストア プロバイダーは、レポートの読み込みの抑制をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="5972b-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="5972b-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5972b-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="5972b-134">_UlFlags_パラメーターで次の互換性のないフラグの組み合わせのいずれかに設定されます。</span><span class="sxs-lookup"><span data-stu-id="5972b-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="5972b-135">SUPPRESS_RECEIPT |CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="5972b-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="5972b-136">SUPPRESS_RECEIPT |CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="5972b-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="5972b-137">CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="5972b-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="5972b-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="5972b-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="5972b-139">呼び出しが成功したが、すべてのメッセージを正常に処理されました。</span><span class="sxs-lookup"><span data-stu-id="5972b-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="5972b-140">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5972b-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="5972b-141">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="5972b-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="5972b-142">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5972b-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5972b-143">注釈</span><span class="sxs-lookup"><span data-stu-id="5972b-143">Remarks</span></span>

<span data-ttu-id="5972b-144">**IMAPIFolder::SetReadFlags**メソッドを設定またはフォルダーのメッセージの 1 つ以上の**PR_MESSAGE_FLAGS**プロパティに MSGFLAG_READ フラグをクリアします。</span><span class="sxs-lookup"><span data-stu-id="5972b-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="5972b-145">開封は必ずしも、目的の受信者がメッセージを読むには実際にメッセージをマークする MSGFLAG_READ フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="5972b-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="5972b-146">**SetReadFlags**リードのレポートの送信を管理します。</span><span class="sxs-lookup"><span data-stu-id="5972b-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="5972b-147">読み取りフラグは、次の変更ことはできません。</span><span class="sxs-lookup"><span data-stu-id="5972b-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="5972b-148">存在しないメッセージです。</span><span class="sxs-lookup"><span data-stu-id="5972b-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="5972b-149">されているメッセージは、他の場所を移動します。</span><span class="sxs-lookup"><span data-stu-id="5972b-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="5972b-150">読み取り/書き込み権限で開かれているメッセージです。</span><span class="sxs-lookup"><span data-stu-id="5972b-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="5972b-151">現在送信されるメッセージです。</span><span class="sxs-lookup"><span data-stu-id="5972b-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="5972b-152">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="5972b-152">Notes to implementers</span></span>

<span data-ttu-id="5972b-153">レポートの読み取りと読み取りのレポートを非表示にする要求の送信をサポートしないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="5972b-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="5972b-154">リードのレポートを抑制することを避けるため、 _ulFlags_パラメーターを設定する SUPPRESS_RECEIPT と**SetReadFlags**が呼び出されたときに MAPI_E_NO_SUPPRESS を返します。</span><span class="sxs-lookup"><span data-stu-id="5972b-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="5972b-155">_LpMsgList_パラメーターは、複数のメッセージをポイントしているときに、できるだけ完全に各メッセージの操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="5972b-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="5972b-156">メモリが不足している、ディスク領域、またはメッセージ ・ ストア内の破損が不足しているなど、ユーザーが制御できない障害が発生した場合を除きは、処理の途中で操作を停止しません。</span><span class="sxs-lookup"><span data-stu-id="5972b-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="5972b-157">_UlFlags_パラメーターでは、どのフラグが設定されている場合は、次の規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="5972b-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="5972b-158">MSGFLAG_READ は既に設定されている場合は機能しません。</span><span class="sxs-lookup"><span data-stu-id="5972b-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="5972b-159">MSGFLAG_READ が設定されていない場合それをすぐに設定し、 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されている場合は、保留中の読み取りのレポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="5972b-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="5972b-160">SUPPRESS_RECEIPT フラグが設定されている場合は、次の規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="5972b-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="5972b-161">MSGFLAG_READ は既に設定されている場合は機能しません。</span><span class="sxs-lookup"><span data-stu-id="5972b-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="5972b-162">MSGFLAG_READ が設定されていない場合は、それを設定し、保留中の読み取りのレポートをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="5972b-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="5972b-163">CLEAR_READ_FLAG フラグを設定すると各メッセージの**PR_MESSAGE_FLAGS**プロパティに MSGFLAG_READ フラグをオフに、読み取りのレポートを送信しません。</span><span class="sxs-lookup"><span data-stu-id="5972b-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="5972b-164">GENERATE_RECEIPT_ONLY フラグが設定されている場合は、すべての保留中の読み取りレポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="5972b-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="5972b-165">MSGFLAG_READ を設定したりクリアの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="5972b-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="5972b-166">SUPPRESS_RECEIPT と GENERATE_RECEIPT_ONLY の両方のフラグが設定されている場合設定**PR_READ_RECEIPT_REQUESTED** FALSE に設定されている場合、読み取りのレポートを送信しません。</span><span class="sxs-lookup"><span data-stu-id="5972b-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5972b-167">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5972b-167">Notes to callers</span></span>

<span data-ttu-id="5972b-168">次の条件下で、これらの戻り値を期待してください。</span><span class="sxs-lookup"><span data-stu-id="5972b-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="5972b-169">**条件**</span><span class="sxs-lookup"><span data-stu-id="5972b-169">**Condition**</span></span>|<span data-ttu-id="5972b-170">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="5972b-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5972b-171">**SetReadFlags**では、すべてのメッセージが正常に処理します。</span><span class="sxs-lookup"><span data-stu-id="5972b-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="5972b-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="5972b-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="5972b-173">**SetReadFlags**は、すべてのメッセージを正常に処理できませんでした。</span><span class="sxs-lookup"><span data-stu-id="5972b-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="5972b-174">MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5972b-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="5972b-175">**SetReadFlags**は完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="5972b-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="5972b-176">MAPI_E_NOT_FOUND を除くエラー値</span><span class="sxs-lookup"><span data-stu-id="5972b-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="5972b-177">**SetReadFlags**が完了することではない場合と仮定しないでその作業は実行されませんでした。</span><span class="sxs-lookup"><span data-stu-id="5972b-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="5972b-178">**SetReadFlags**を設定または 1 つまたは複数のメッセージのエラーが発生する前に MSGFLAG_READ フラグをオフにすることされている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5972b-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5972b-179">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="5972b-179">MFCMAPI reference</span></span>

<span data-ttu-id="5972b-180">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="5972b-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5972b-181">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="5972b-181">**File**</span></span>|<span data-ttu-id="5972b-182">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="5972b-182">**Function**</span></span>|<span data-ttu-id="5972b-183">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="5972b-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5972b-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="5972b-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="5972b-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="5972b-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="5972b-186">MFCMAPI では、 **IMAPIFolder::SetReadFlags**メソッドを使用して、指定されたメッセージの読み取り状態を手動で設定します。</span><span class="sxs-lookup"><span data-stu-id="5972b-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5972b-187">関連項目</span><span class="sxs-lookup"><span data-stu-id="5972b-187">See also</span></span>

- [<span data-ttu-id="5972b-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="5972b-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="5972b-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="5972b-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="5972b-190">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5972b-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="5972b-191">PidTagReadReceiptRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5972b-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="5972b-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5972b-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- <span data-ttu-id="5972b-193">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="5972b-193">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>  
- [<span data-ttu-id="5972b-194">エラー処理のためのマクロの使用</span><span class="sxs-lookup"><span data-stu-id="5972b-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

