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
# <a name="imessagesetreadflag"></a><span data-ttu-id="b637b-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="b637b-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="b637b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b637b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b637b-105">メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグを設定またはクリアし、閲覧レポートの送信を管理します。</span><span class="sxs-lookup"><span data-stu-id="b637b-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b637b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b637b-106">Parameters</span></span>

<span data-ttu-id="b637b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b637b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b637b-108">順番メッセージの読み取りフラグの設定を制御するフラグのビットマスクです。このフラグは、メッセージの MSGFLAG_READ フラグが**PR_MESSAGE_FLAGS**プロパティで、開封レポートの処理になります。</span><span class="sxs-lookup"><span data-stu-id="b637b-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="b637b-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b637b-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="b637b-110">CLEAR_READ_FLAG: MSGFLAG_READ フラグは**PR_MESSAGE_FLAGS**でクリアされ、閲覧レポートは送信されません。</span><span class="sxs-lookup"><span data-stu-id="b637b-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="b637b-111">CLEAR_NRN_PENDING: MSGFLAG_NRN_PENDING フラグは**PR_MESSAGE_FLAGS**ではクリアされ、非開封レポートは送信されないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b637b-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="b637b-112">CLEAR_RN_PENDING: MSGFLAG_RN_PENDING フラグは**PR_MESSAGE_FLAGS**でクリアされ、閲覧レポートは送信されません。</span><span class="sxs-lookup"><span data-stu-id="b637b-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="b637b-113">GENERATE_RECEIPT_ONLY: 読み取りレポートは、保留中の場合は送信されますが、MSGFLAG_READ フラグの状態は変更されません。</span><span class="sxs-lookup"><span data-stu-id="b637b-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="b637b-114">MAPI_DEFERRED_ERRORS: **setreadflag**が正常に返されるようにします。操作が完了する前である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b637b-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="b637b-115">SUPPRESS_RECEIPT: 読み取りレポートが要求されている場合は、保留中の読み取りレポートを取り消す必要があります。この呼び出しは、メッセージの状態を未読から読み取りに変更します。</span><span class="sxs-lookup"><span data-stu-id="b637b-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="b637b-116">この呼び出しでメッセージの状態が変更されない場合、メッセージストアプロバイダーはこのフラグを無視できます。</span><span class="sxs-lookup"><span data-stu-id="b637b-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b637b-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="b637b-117">Return value</span></span>

<span data-ttu-id="b637b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b637b-118">S_OK</span></span> 
  
> <span data-ttu-id="b637b-119">メッセージの read フラグが正常に設定またはクリアされました。</span><span class="sxs-lookup"><span data-stu-id="b637b-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="b637b-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="b637b-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="b637b-121">メッセージストアプロバイダーは、閲覧レポートの抑制をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b637b-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="b637b-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b637b-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="b637b-123">次のフラグの組み合わせのいずれかが_ulflags_パラメーターで設定されています。</span><span class="sxs-lookup"><span data-stu-id="b637b-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="b637b-124">SUPPRESS_RECEIPT |CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="b637b-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="b637b-125">SUPPRESS_RECEIPT |CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="b637b-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="b637b-126">CLEAR_READ_FLAG |GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="b637b-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b637b-127">注釈</span><span class="sxs-lookup"><span data-stu-id="b637b-127">Remarks</span></span>

<span data-ttu-id="b637b-128">**IMessage:: setreadflag**メソッドは、 **PR_MESSAGE_FLAGS**プロパティのメッセージの MSGFLAG_READ フラグを設定またはクリアし、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)を呼び出してメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="b637b-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="b637b-129">MSGFLAG_READ フラグを設定すると、メッセージは開封済みとしてマークされます。これは、意図した受信者が実際にメッセージを読んでいることを示すわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b637b-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="b637b-130">**setreadflags**は、閲覧レポートの送信も管理します。</span><span class="sxs-lookup"><span data-stu-id="b637b-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="b637b-131">閲覧レポートが送信されるのは、送信者が1人を要求した場合のみです。</span><span class="sxs-lookup"><span data-stu-id="b637b-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="b637b-132">読み取りフラグは次のように変更できません。</span><span class="sxs-lookup"><span data-stu-id="b637b-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="b637b-133">存在しないメッセージ。</span><span class="sxs-lookup"><span data-stu-id="b637b-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="b637b-134">他の場所に移動されたメッセージ。</span><span class="sxs-lookup"><span data-stu-id="b637b-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="b637b-135">読み取り/書き込みアクセス許可で開いているメッセージ。</span><span class="sxs-lookup"><span data-stu-id="b637b-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="b637b-136">現在送信されているメッセージ。</span><span class="sxs-lookup"><span data-stu-id="b637b-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="b637b-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b637b-137">Notes to callers</span></span>

<span data-ttu-id="b637b-138">_ulflags_パラメーターにどのフラグも設定されていない場合は、次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="b637b-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="b637b-139">MSGFLAG_READ が既に設定されている場合は、何も実行しません。</span><span class="sxs-lookup"><span data-stu-id="b637b-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="b637b-140">MSGFLAG_READ が設定されていない場合は、 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されている場合は設定し、保留中の読み取りレポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="b637b-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="b637b-141">SUPPRESS_RECEIPT と GENERATE_RECEIPT_ONLY の両方のフラグが設定されている場合は、PR_READ_RECEIPT_REQUESTED ビット (設定されている場合) をクリアし、閲覧レポートを送信しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b637b-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="b637b-142">SUPPRESS_RECEIPT フラグが設定されている場合:</span><span class="sxs-lookup"><span data-stu-id="b637b-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="b637b-143">MSGFLAG_READ が既に設定されている場合は、何も実行しません。</span><span class="sxs-lookup"><span data-stu-id="b637b-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="b637b-144">MSGFLAG_READ が設定されていない場合は、設定し、保留中のすべての開封レポートを取り消します。</span><span class="sxs-lookup"><span data-stu-id="b637b-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="b637b-145">CLEAR_READ_FLAG フラグが設定されている場合は、各メッセージの**PR_MESSAGE_FLAGS**プロパティの MSGFLAG_READ フラグをオフにして、読み取りレポートを送信しないようにします。</span><span class="sxs-lookup"><span data-stu-id="b637b-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="b637b-146">GENERATE_RECEIPT_ONLY フラグが設定されている場合は、保留中のすべての読み取りレポートを送信します。</span><span class="sxs-lookup"><span data-stu-id="b637b-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="b637b-147">MSGFLAG_READ を設定またはクリアしません。</span><span class="sxs-lookup"><span data-stu-id="b637b-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="b637b-148">SUPPRESS_RECEIPT と GENERATE_RECEIPT_ONLY の両方のフラグが設定されている場合は、PR_READ_RECEIPT_REQUESTED プロパティが設定されている場合は FALSE に設定し、閲覧レポートを送信しないようにします。</span><span class="sxs-lookup"><span data-stu-id="b637b-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="b637b-149">特定の条件下での読み取りレポートの生成を抑制することで、レポートの動作を最適化できます。</span><span class="sxs-lookup"><span data-stu-id="b637b-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="b637b-150">ただし、レポートの抑制をサポートしておらず、クライアントが SUPPRESS_RECEIPT フラグを設定して**setreadflag**を呼び出している場合は、MAPI_E_NO_SUPPRESS を返します。</span><span class="sxs-lookup"><span data-stu-id="b637b-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b637b-151">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="b637b-151">MFCMAPI reference</span></span>

<span data-ttu-id="b637b-152">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b637b-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b637b-153">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="b637b-153">**File**</span></span>|<span data-ttu-id="b637b-154">**関数**</span><span class="sxs-lookup"><span data-stu-id="b637b-154">**Function**</span></span>|<span data-ttu-id="b637b-155">**コメント**</span><span class="sxs-lookup"><span data-stu-id="b637b-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b637b-156">folderdlg</span><span class="sxs-lookup"><span data-stu-id="b637b-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="b637b-157">cfolderdlg:: OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="b637b-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="b637b-158">mfcmapi は、 **IMessage:: setreadflag**メソッドを使用して、選択されたメッセージに対する読み取りフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="b637b-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b637b-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="b637b-159">See also</span></span>

- [<span data-ttu-id="b637b-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b637b-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="b637b-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="b637b-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="b637b-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="b637b-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="b637b-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="b637b-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="b637b-164">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b637b-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="b637b-165">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b637b-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- <span data-ttu-id="b637b-166">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b637b-166">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

