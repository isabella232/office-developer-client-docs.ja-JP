---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439871"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="8e8f7-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="8e8f7-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="8e8f7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e8f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e8f7-105">メッセージの MSGFLAG_READ ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ **PR_MESSAGE_FLAGS** フラグを設定またはクリアし、読み取りレポートの送信を管理します。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8e8f7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8e8f7-106">Parameters</span></span>

<span data-ttu-id="8e8f7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e8f7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8e8f7-108">[in]メッセージの読み取りフラグの設定 **(PR_MESSAGE_FLAGS** プロパティのメッセージの MSGFLAG_READ フラグ、および読み取りレポートの処理を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="8e8f7-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="8e8f7-110">CLEAR_READ_FLAG: MSGFLAG_READフラグは、PR_MESSAGE_FLAGSでクリアし、読み取 **り** レポートを送信する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="8e8f7-111">CLEAR_NRN_PENDING: MSGFLAG_NRN_PENDINGフラグは、PR_MESSAGE_FLAGSでクリアする必要があります。読み取り以外のレポートを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="8e8f7-112">CLEAR_RN_PENDING: MSGFLAG_RN_PENDINGフラグは、PR_MESSAGE_FLAGSでクリアし、読み取 **り** レポートを送信する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="8e8f7-113">GENERATE_RECEIPT_ONLY: 保留中の場合は読み取りレポートを送信する必要がありますが、このフラグの状態に変更MSGFLAG_READがあります。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="8e8f7-114">MAPI_DEFERRED_ERRORS: 操作が完了する前に **、SetReadFlag** を正常に返します。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="8e8f7-115">SUPPRESS_RECEIPT: 読み取りレポートが要求され、この呼び出しによってメッセージの状態が未読から読み取りに変更された場合は、保留中の読み取りレポートを取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="8e8f7-116">この呼び出しでメッセージの状態が変更されない場合、メッセージ ストア プロバイダーは、このフラグを無視できます。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8e8f7-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="8e8f7-117">Return value</span></span>

<span data-ttu-id="8e8f7-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e8f7-118">S_OK</span></span> 
  
> <span data-ttu-id="8e8f7-119">メッセージの読み取りフラグが正常に設定またはクリアされました。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="8e8f7-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="8e8f7-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="8e8f7-121">メッセージ ストア プロバイダーは、読み取りレポートの抑制をサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="8e8f7-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8e8f7-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="8e8f7-123">ulFlags パラメーターには、次のいずれかのフラグの組  _み合わせが設定_ されています。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="8e8f7-124">SUPPRESS_RECEIPT |CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="8e8f7-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="8e8f7-125">SUPPRESS_RECEIPT |CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="8e8f7-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="8e8f7-126">CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="8e8f7-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e8f7-127">注釈</span><span class="sxs-lookup"><span data-stu-id="8e8f7-127">Remarks</span></span>

<span data-ttu-id="8e8f7-128">**IMessage::SetReadFlag** メソッドは **、PR_MESSAGE_FLAGS** プロパティでメッセージの MSGFLAG_READ フラグを設定またはクリアし [、IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出してメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="8e8f7-129">MSGFLAG_READフラグを設定すると、メッセージが読み取りされたとマークされます。これは、意図した受信者が実際にメッセージを読み取ったとは限りません。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="8e8f7-130">**SetReadFlags は、** 読み取りレポートの送信も管理します。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="8e8f7-131">読み取りレポートは、送信者が要求した場合にのみ送信されます。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="8e8f7-132">読み取りフラグは、次の場合に変更できません。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="8e8f7-133">存在しないメッセージ。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="8e8f7-134">他の場所に移動されたメッセージ。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="8e8f7-135">読み取り/書き込み権限で開いているメッセージ。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="8e8f7-136">現在送信されているメッセージ。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="8e8f7-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="8e8f7-137">Notes to callers</span></span>

<span data-ttu-id="8e8f7-138">_ulFlags_ パラメーターにフラグが設定されない場合は、次の規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="8e8f7-139">既MSGFLAG_READ設定されている場合は、何も行いません。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="8e8f7-140">このMSGFLAG_READ設定されていない場合は、PR_READ_RECEIPT_REQUESTED **(** [PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されている場合は、それを設定し、保留中の読み取りレポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="8e8f7-141">SUPPRESS_RECEIPT フラグと GENERATE_RECEIPT_ONLY フラグの両方が設定されている場合、PR_READ_RECEIPT_REQUESTED ビットを設定するとクリアされ、読み取りレポートは送信されません。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="8e8f7-142">このフラグSUPPRESS_RECEIPT設定されている場合は、次の条件を実行します。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="8e8f7-143">既MSGFLAG_READ設定されている場合は、何も行いません。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="8e8f7-144">このMSGFLAG_READ設定されていない場合は、設定し、保留中の読み取りレポートを取り消します。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="8e8f7-145">このフラグCLEAR_READ_FLAG設定されている場合は、各メッセージの MSGFLAG_READ プロパティの PR_MESSAGE_FLAGS フラグをクリアし、読み取りレポートを送信しない。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="8e8f7-146">このフラグGENERATE_RECEIPT_ONLY設定されている場合は、保留中の読み取りレポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="8e8f7-147">設定または削除を行MSGFLAG_READ。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="8e8f7-148">SUPPRESS_RECEIPT フラグと GENERATE_RECEIPT_ONLY フラグの両方が設定されている場合は、PR_READ_RECEIPT_REQUESTED プロパティを FALSE に設定し、読み取りレポートを送信しない場合は FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="8e8f7-149">特定の条件下で読み取りレポートの生成を抑制することで、レポートの動作を最適化できます。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="8e8f7-150">ただし、レポートの抑制をサポートしていない場合に、クライアントが **setReadFlag** を呼び出し、SUPPRESS_RECEIPTフラグを設定した場合は、MAPI_E_NO_SUPPRESS。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8e8f7-151">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="8e8f7-151">MFCMAPI reference</span></span>

<span data-ttu-id="8e8f7-152">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8e8f7-153">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="8e8f7-153">**File**</span></span>|<span data-ttu-id="8e8f7-154">**関数**</span><span class="sxs-lookup"><span data-stu-id="8e8f7-154">**Function**</span></span>|<span data-ttu-id="8e8f7-155">**コメント**</span><span class="sxs-lookup"><span data-stu-id="8e8f7-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8e8f7-156">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="8e8f7-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="8e8f7-157">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="8e8f7-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="8e8f7-158">MFCMAPI は **、IMessage::SetReadFlag** メソッドを使用して、選択したメッセージに対して読み取りフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="8e8f7-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e8f7-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e8f7-159">See also</span></span>

- [<span data-ttu-id="8e8f7-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="8e8f7-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="8e8f7-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="8e8f7-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="8e8f7-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="8e8f7-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="8e8f7-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8e8f7-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="8e8f7-164">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e8f7-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="8e8f7-165">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8e8f7-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- <span data-ttu-id="8e8f7-166">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="8e8f7-166">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

