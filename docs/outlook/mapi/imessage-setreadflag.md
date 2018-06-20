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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0ae35166f01f597c2c3ab399a1b66e5760ab0dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800896"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="ae6fb-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="ae6fb-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="ae6fb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ae6fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ae6fb-105">設定し、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティに MSGFLAG_READ フラグをクリアまたはリードのレポートの送信を管理します。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ae6fb-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="ae6fb-106">Parameters</span></span>

<span data-ttu-id="ae6fb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ae6fb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ae6fb-108">[in]メッセージの読み取りの設定を制御するフラグのビットマスクのフラグは、その**PR_MESSAGE_FLAGS**プロパティは、読み取りのレポートの処理に MSGFLAG_READ フラグをメッセージの。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="ae6fb-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="ae6fb-110">CLEAR_READ_FLAG: **PR_MESSAGE_FLAGS**に MSGFLAG_READ フラグをクリアする必要があり、リードのレポートを送信しません。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="ae6fb-111">CLEAR_NRN_PENDING: **PR_MESSAGE_FLAGS**に MSGFLAG_NRN_PENDING フラグをクリアする必要があり、未開封レポートを送信しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="ae6fb-112">CLEAR_RN_PENDING: **PR_MESSAGE_FLAGS**に MSGFLAG_RN_PENDING フラグをクリアする必要があり、リードのレポートを送信しません。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="ae6fb-113">GENERATE_RECEIPT_ONLY: 1 つは、保留中が存在しないはずの MSGFLAG_READ フラグの状態の変更は、リードのレポートを送信してください。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="ae6fb-114">MAPI_DEFERRED_ERRORS: 正常に完了可能性がありますが、操作を完了する前にするには**SetReadFlag**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="ae6fb-115">SUPPRESS_RECEIPT: 要求された読み取りのレポートと、この呼び出しからの読み取りに未読のメッセージの状態を変更する場合は、保留中の読み取りレポートをキャンセルするか。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="ae6fb-116">この呼び出しで、メッセージの状態が変化しない場合、メッセージ ストア プロバイダーは、このフラグを無視できます。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ae6fb-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ae6fb-117">Return value</span></span>

<span data-ttu-id="ae6fb-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae6fb-118">S_OK</span></span> 
  
> <span data-ttu-id="ae6fb-119">読み取りフラグは正常に設定またはクリアされました。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="ae6fb-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="ae6fb-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="ae6fb-121">メッセージ ストア プロバイダーは、レポートの読み込みの抑制をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="ae6fb-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ae6fb-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="ae6fb-123">_UlFlags_パラメーターで次のフラグの組み合わせのいずれかに設定されます。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="ae6fb-124">SUPPRESS_RECEIPT |CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="ae6fb-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="ae6fb-125">SUPPRESS_RECEIPT |CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="ae6fb-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="ae6fb-126">CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="ae6fb-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae6fb-127">備考</span><span class="sxs-lookup"><span data-stu-id="ae6fb-127">Remarks</span></span>

<span data-ttu-id="ae6fb-128">**IMessage::SetReadFlag**メソッドを設定または、 **PR_MESSAGE_FLAGS**プロパティと、メッセージを保存するのには[IMAPIProp::SaveChanges](imapiprop-savechanges.md)の呼び出しでのメッセージの MSGFLAG_READ フラグをクリアします。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="ae6fb-129">MSGFLAG_READ フラグを設定は、必ずしも目的の受信者がメッセージを読むには実際には、読み取りとメッセージをマークします。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="ae6fb-130">**SetReadFlags**リードのレポートの送信を管理します。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="ae6fb-131">いずれかの送信者が要求された場合のみ、読み取りのレポートが送信されます。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="ae6fb-132">読み取りフラグを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="ae6fb-133">存在しないメッセージです。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="ae6fb-134">されているメッセージは、他の場所を移動します。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="ae6fb-135">読み取り/書き込み権限で開かれているメッセージです。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="ae6fb-136">現在送信されるメッセージです。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="ae6fb-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ae6fb-137">Notes to callers</span></span>

<span data-ttu-id="ae6fb-138">_UlFlags_パラメーターでは、どのフラグが設定されている場合は、次の規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="ae6fb-139">MSGFLAG_READ は既に設定されている場合は機能しません。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="ae6fb-140">MSGFLAG_READ が設定されていない場合は、それを設定し、 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されている場合は、保留中の読み取りのレポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="ae6fb-141">SUPPRESS_RECEIPT と GENERATE_RECEIPT_ONLY の両方のフラグが設定されている場合、PR_READ_RECEIPT_REQUESTED ビットの場合はこのオプションを設定すると、クリアする必要があり、リードのレポートは送信されませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="ae6fb-142">SUPPRESS_RECEIPT フラグを設定するとします。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="ae6fb-143">MSGFLAG_READ は既に設定されている場合は機能しません。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="ae6fb-144">MSGFLAG_READ が設定されていない場合は、それを設定し、保留中の読み取りのレポートをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="ae6fb-145">CLEAR_READ_FLAG フラグを設定すると各メッセージの**PR_MESSAGE_FLAGS**プロパティに MSGFLAG_READ フラグをオフに、読み取りのレポートを送信しません。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="ae6fb-146">GENERATE_RECEIPT_ONLY フラグが設定されている場合は、すべての保留中の読み取りレポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="ae6fb-147">MSGFLAG_READ を設定したりクリアの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="ae6fb-148">SUPPRESS_RECEIPT と GENERATE_RECEIPT_ONLY の両方のフラグが設定されているときにプロパティを設定、PR_READ_RECEIPT_REQUESTED FALSE に設定されている場合、読み取りのレポートを送信しません。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="ae6fb-149">特定の条件下でのリードのレポートの生成を抑制することによって、レポートの動作を最適化できます。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="ae6fb-150">ただし、レポートの抑制をサポートしていないクライアントは、SUPPRESS_RECEIPT フラグを設定して**SetReadFlag**を呼び出す場合は、MAPI_E_NO_SUPPRESS を取得します。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ae6fb-151">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ae6fb-151">MFCMAPI reference</span></span>

<span data-ttu-id="ae6fb-152">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ae6fb-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ae6fb-153">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ae6fb-153">**File**</span></span>|<span data-ttu-id="ae6fb-154">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ae6fb-154">**Function**</span></span>|<span data-ttu-id="ae6fb-155">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ae6fb-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ae6fb-156">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ae6fb-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="ae6fb-157">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="ae6fb-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="ae6fb-158">MFCMAPI では、 **IMessage::SetReadFlag**メソッドを使用して、選択したメッセージに開封のフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="ae6fb-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae6fb-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae6fb-159">See also</span></span>

- [<span data-ttu-id="ae6fb-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ae6fb-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="ae6fb-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="ae6fb-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="ae6fb-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="ae6fb-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="ae6fb-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="ae6fb-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="ae6fb-164">PidTagMessageFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ae6fb-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="ae6fb-165">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ae6fb-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- <span data-ttu-id="ae6fb-166">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ae6fb-166">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

