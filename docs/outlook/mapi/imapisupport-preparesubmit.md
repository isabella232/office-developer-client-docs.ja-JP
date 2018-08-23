---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5f45a6457bba738b290d967260bbd34c0f88f93f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595063"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="01ceb-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="01ceb-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="01ceb-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01ceb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01ceb-105">MAPI スプーラーに送信するためには、メッセージを準備します。</span><span class="sxs-lookup"><span data-stu-id="01ceb-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="01ceb-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="01ceb-106">Parameters</span></span>

 <span data-ttu-id="01ceb-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="01ceb-107">_lpMessage_</span></span>
  
> <span data-ttu-id="01ceb-108">[in]準備するのには、メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="01ceb-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="01ceb-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="01ceb-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="01ceb-110">[で [チェック アウト]入力では、 _lpulFlags_パラメーターは予約されており、0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="01ceb-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="01ceb-111">出力では、 _lpulFlags_は NULL にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="01ceb-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="01ceb-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="01ceb-112">Return value</span></span>

<span data-ttu-id="01ceb-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="01ceb-113">S_OK</span></span> 
  
> <span data-ttu-id="01ceb-114">メッセージの準備ができました。</span><span class="sxs-lookup"><span data-stu-id="01ceb-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01ceb-115">注釈</span><span class="sxs-lookup"><span data-stu-id="01ceb-115">Remarks</span></span>

<span data-ttu-id="01ceb-116">メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::PrepareSubmit**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="01ceb-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="01ceb-117">メッセージ ストア プロバイダーは、MAPI スプーラーに送信するためのメッセージを準備するのには[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドの実装では、 **PrepareSubmit**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01ceb-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="01ceb-118">**PrepareSubmit**は、MSGFLAG_RESEND フラグが、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティで設定されたメッセージを処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="01ceb-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="01ceb-119">MSGFLAG_RESEND は、最初の送信が失敗したときに再送信する要求を含むメッセージに設定されています。</span><span class="sxs-lookup"><span data-stu-id="01ceb-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="01ceb-120">メッセージを正常に受信する受信者の一覧で受信者の指定しませんでしたが、 **PrepareSubmit**が決定します。</span><span class="sxs-lookup"><span data-stu-id="01ceb-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="01ceb-121">受信者の一覧にアクセスするには、 **PrepareSubmit**は、メッセージの[IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01ceb-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="01ceb-122">受信者のデータを取得するのには、 **PrepareSubmit**は、受信者テーブルの[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01ceb-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="01ceb-123">テーブル内の各行の**PrepareSubmit**は**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) のプロパティをチェックし、次の操作のいずれか。</span><span class="sxs-lookup"><span data-stu-id="01ceb-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="01ceb-124">MAPI_SUBMITTED フラグが設定されている場合、 **PrepareSubmit**はフラグをクリアし、**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="01ceb-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="01ceb-125">MAPI_SUBMITTED フラグが設定されていない場合、 **PrepareSubmit**は**PR_RECIPIENT_TYPE**を MAPI_P1 に変更し、true を指定する**れない**を設定します。</span><span class="sxs-lookup"><span data-stu-id="01ceb-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="01ceb-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="01ceb-126">Notes to callers</span></span>

<span data-ttu-id="01ceb-127">**PrepareSubmit**を呼び出すと、前に、 [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出したあり、 _ulFlags_パラメーターに NOTIFY_READYTOSEND フラグを設定することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="01ceb-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="01ceb-128">**SpoolerNotify**の呼び出しは、 **PrepareSubmit**への呼び出しの前にセッションごとに 1 回行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="01ceb-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="01ceb-129">**SpoolerNotify**では、MAPI スプーラーを同期し、により、ログオンしているすべての必要なトランスポート プロバイダーのアドレスの種類を登録します。</span><span class="sxs-lookup"><span data-stu-id="01ceb-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01ceb-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="01ceb-130">See also</span></span>



[<span data-ttu-id="01ceb-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="01ceb-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="01ceb-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="01ceb-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="01ceb-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="01ceb-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

