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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349232"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="37bae-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="37bae-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="37bae-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37bae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37bae-105">すべてのメッセージのプロパティを保存し、メッセージを送信する準備が整ったことをマークします。</span><span class="sxs-lookup"><span data-stu-id="37bae-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="37bae-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37bae-106">Parameters</span></span>

 <span data-ttu-id="37bae-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="37bae-107">_ulFlags_</span></span>
  
> <span data-ttu-id="37bae-108">順番メッセージの送信方法を制御するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="37bae-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="37bae-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="37bae-109">The following flag can be set:</span></span>
    
<span data-ttu-id="37bae-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="37bae-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="37bae-111">MAPI はメッセージを直ちに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37bae-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="37bae-112">このフラグは現在使用されていません。</span><span class="sxs-lookup"><span data-stu-id="37bae-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37bae-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="37bae-113">Return value</span></span>

<span data-ttu-id="37bae-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="37bae-114">S_OK</span></span> 
  
> <span data-ttu-id="37bae-115">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="37bae-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="37bae-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="37bae-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="37bae-117">メッセージの recipient テーブルが空です。</span><span class="sxs-lookup"><span data-stu-id="37bae-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37bae-118">解説</span><span class="sxs-lookup"><span data-stu-id="37bae-118">Remarks</span></span>

<span data-ttu-id="37bae-119">**IMessage:: submitmessage**メソッドは、メッセージを送信する準備が整ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="37bae-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="37bae-120">MAPI は、メッセージが送信をマークされている順序で、基になるメッセージングシステムにメッセージを渡します。</span><span class="sxs-lookup"><span data-stu-id="37bae-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="37bae-121">この機能により、メッセージは、基礎となるメッセージングシステムが責任を持つ前に、しばらくの間メッセージストアに保持される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="37bae-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="37bae-122">宛先での受信の順序は、基になるメッセージングシステムのコントロール内にあり、メッセージが送信された順序とは必ずしも一致しません。</span><span class="sxs-lookup"><span data-stu-id="37bae-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="37bae-123">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="37bae-123">Notes to implementers</span></span>

<span data-ttu-id="37bae-124">メッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して保存し、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="37bae-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="37bae-125">MSGFLAG_RESEND フラグが設定されている場合は、次のように呼び出し imapisupport を呼び出します。 [:P reparesubmit](imapisupport-preparesubmit.md)。</span><span class="sxs-lookup"><span data-stu-id="37bae-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="37bae-126">**PrepareSubmit**は、再送信メッセージ内のすべての受信者の受信者の種類と**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="37bae-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="37bae-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="37bae-127">Notes to callers</span></span>

<span data-ttu-id="37bae-128">**submitmessage**が戻ると、そのメッセージへのすべてのポインターと、それに関連付けられているサブオブジェクトメッセージ、フォルダー、添付ファイル、ストリーム、テーブルなどが無効になります。</span><span class="sxs-lookup"><span data-stu-id="37bae-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="37bae-129">MAPI では、これらのポインターに対して他の操作を行うことはできません。ただし、 **IUnknown:: Release**メソッドを呼び出すことはありません。</span><span class="sxs-lookup"><span data-stu-id="37bae-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="37bae-130">MAPI は、 **submitmessage**を呼び出した後、メッセージとすべての関連するサブオブジェクトを解放する必要があるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="37bae-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="37bae-131">ただし、 **submitmessage**から不足または無効な情報を示すエラー値が返された場合、メッセージは開いたままになり、ポインターは有効なままとなります。</span><span class="sxs-lookup"><span data-stu-id="37bae-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="37bae-132">送信操作を取り消すには、メッセージが送信される前に、メッセージの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティへのポインターを取得して保存します。</span><span class="sxs-lookup"><span data-stu-id="37bae-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="37bae-133">メッセージのエントリ id は、メッセージの送信後に無効になるため、 **submitmessage**を呼び出す前に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37bae-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="37bae-134">送信を取り消すには、 _lな tryid_パラメーターをこのエントリ識別子にポイントし、 [IMsgStore:: abortsubmit](imsgstore-abortsubmit.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="37bae-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="37bae-135">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="37bae-135">MFCMAPI reference</span></span>

<span data-ttu-id="37bae-136">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37bae-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="37bae-137">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="37bae-137">**File**</span></span>|<span data-ttu-id="37bae-138">**関数**</span><span class="sxs-lookup"><span data-stu-id="37bae-138">**Function**</span></span>|<span data-ttu-id="37bae-139">**コメント**</span><span class="sxs-lookup"><span data-stu-id="37bae-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37bae-140">folderdlg</span><span class="sxs-lookup"><span data-stu-id="37bae-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="37bae-141">**cfolderdlg:: onsubmitmessage**</span><span class="sxs-lookup"><span data-stu-id="37bae-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="37bae-142">mfcmapi は、 **IMessage:: submitmessage**メソッドを使用して、選択されたメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="37bae-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37bae-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="37bae-143">See also</span></span>



[<span data-ttu-id="37bae-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="37bae-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="37bae-145">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="37bae-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


<span data-ttu-id="37bae-146">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="37bae-146">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

