---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437365"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="0e5f8-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="0e5f8-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="0e5f8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e5f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e5f8-105">メッセージのすべてのプロパティを保存し、メッセージを送信準備完了としてマークします。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0e5f8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e5f8-106">Parameters</span></span>

 <span data-ttu-id="0e5f8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0e5f8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0e5f8-108">[in]メッセージの送信方法を制御するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="0e5f8-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0e5f8-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="0e5f8-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="0e5f8-111">MAPI は、すぐにメッセージを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="0e5f8-112">このフラグは現在使用されていない。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0e5f8-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e5f8-113">Return value</span></span>

<span data-ttu-id="0e5f8-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e5f8-114">S_OK</span></span> 
  
> <span data-ttu-id="0e5f8-115">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="0e5f8-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0e5f8-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="0e5f8-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="0e5f8-117">メッセージの受信者テーブルが空です。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e5f8-118">注釈</span><span class="sxs-lookup"><span data-stu-id="0e5f8-118">Remarks</span></span>

<span data-ttu-id="0e5f8-119">**IMessage::SubmitMessage** メソッドは、メッセージを送信する準備ができているとマークします。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="0e5f8-120">MAPI は、基になるメッセージング システムに、メッセージが送信用にマークされている順序でメッセージを渡します。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="0e5f8-121">この機能により、基になるメッセージング システムがメッセージ を処理する前に、メッセージがメッセージ ストアに一時残る場合があります。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="0e5f8-122">宛先での受信の順序は、基になるメッセージング システムのコントロール内にあるため、メッセージが送信された順序と必ずしも一致しません。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0e5f8-123">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="0e5f8-123">Notes to implementers</span></span>

<span data-ttu-id="0e5f8-124">メッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出して保存し、メッセージの PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="0e5f8-125">このフラグMSGFLAG_RESEND設定されている場合は [、IMAPISupport::P repareSubmit を呼び出します](imapisupport-preparesubmit.md)。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="0e5f8-126">**PrepareSubmit は** 、再送信メッセージ内 **PR_RESPONSIBILITY** 受信者の受信者の種類とプロパティ [(PidTagResponsibility)](pidtagresponsibility-canonical-property.md)を更新します。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0e5f8-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0e5f8-127">Notes to callers</span></span>

<span data-ttu-id="0e5f8-128">**SubmitMessage が** 返される場合、メッセージとその関連付けられたサブオブジェクトメッセージ、フォルダー、添付ファイル、ストリーム、テーブルなどへのすべてのポインターは無効になります。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="0e5f8-129">MAPI は **、IUnknown::Release** メソッドを呼び出す以外は、これらのポインターに対するそれ以上の操作を許可しない。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="0e5f8-130">MAPI は **、SubmitMessage** が呼び出された後、メッセージと関連付けられているすべてのサブオブジェクトを解放するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="0e5f8-131">ただし **、SubmitMessage が** 欠落または無効な情報を示すエラー値を返した場合、メッセージは開いたままで、ポインターは有効なままです。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="0e5f8-132">送信操作をキャンセルするには、メッセージが送信される前に、メッセージの PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティへのポインターを取得して格納します。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="0e5f8-133">メッセージのエントリ識別子は、メッセージの送信後に無効になりますので **、SubmitMessage** を呼び出す前に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="0e5f8-134">送信をキャンセルするには  _、lpEntryId_ パラメーターをこのエントリ識別子にポイントし [、IMsgStore::AbortSubmit を呼び出します](imsgstore-abortsubmit.md)。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0e5f8-135">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="0e5f8-135">MFCMAPI reference</span></span>

<span data-ttu-id="0e5f8-136">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0e5f8-137">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="0e5f8-137">**File**</span></span>|<span data-ttu-id="0e5f8-138">**関数**</span><span class="sxs-lookup"><span data-stu-id="0e5f8-138">**Function**</span></span>|<span data-ttu-id="0e5f8-139">**コメント**</span><span class="sxs-lookup"><span data-stu-id="0e5f8-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e5f8-140">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0e5f8-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="0e5f8-141">**CFolderDlg::OnSubmitMessage**</span><span class="sxs-lookup"><span data-stu-id="0e5f8-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="0e5f8-142">MFCMAPI は **、IMessage::SubmitMessage** メソッドを使用して、選択したメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="0e5f8-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e5f8-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e5f8-143">See also</span></span>



[<span data-ttu-id="0e5f8-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="0e5f8-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="0e5f8-145">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0e5f8-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


<span data-ttu-id="0e5f8-146">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0e5f8-146">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

