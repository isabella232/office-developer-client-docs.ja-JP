---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: efeac5a54c576d8b76d94ea7af8949e64dbccab6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588511"
---
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="22530-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="22530-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="22530-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22530-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22530-105">新しいメッセージを初期化します。</span><span class="sxs-lookup"><span data-stu-id="22530-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="22530-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="22530-106">Parameters</span></span>

 <span data-ttu-id="22530-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="22530-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="22530-108">[in]ビューアーでのメッセージを操作するのには、フォームを使用するメッセージのサイトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="22530-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="22530-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="22530-109">_pMessage_</span></span>
  
> <span data-ttu-id="22530-110">[in]新しいメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="22530-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="22530-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="22530-111">Return value</span></span>

<span data-ttu-id="22530-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="22530-112">S_OK</span></span> 
  
> <span data-ttu-id="22530-113">新しいメッセージが正常に初期化しました。</span><span class="sxs-lookup"><span data-stu-id="22530-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="22530-114">注釈</span><span class="sxs-lookup"><span data-stu-id="22530-114">Remarks</span></span>

<span data-ttu-id="22530-115">フォーム ビューアーは、ユーザーがフォームを処理するメッセージ クラスが所属する新しいメッセージを書き込むときに、 **IPersistMessage::InitNew**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="22530-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="22530-116">フォーム オブジェクトに有効なユーザー インターフェイスのポインターがある場合は、メッセージ オブジェクトのユーザー インターフェイスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="22530-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="22530-117">**InitNew**呼び出せませんフォームが[初期化されていない](uninitialized-state.md)状態以外の任意の状態にします。</span><span class="sxs-lookup"><span data-stu-id="22530-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="22530-118">**InitNew**が呼び出されたときに、フォームは他の状態のいずれかでは場合は、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="22530-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="22530-119">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="22530-119">Notes to implementers</span></span>

<span data-ttu-id="22530-120">通常、プロパティが保存されていないメッセージは変更済みとしてマーク、クライアントがユーザーの入力を求めるダイアログ ボックスを表示できるようにこれらのプロパティを保存するかどうか。</span><span class="sxs-lookup"><span data-stu-id="22530-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="22530-121">ユーザーは、メッセージを保存する必要があることを示している場合は、データを保存し、クリーンとしてメッセージをマーク、正常終了します。</span><span class="sxs-lookup"><span data-stu-id="22530-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="22530-122">ただし、新たに初期化されたメッセージの処理は、いずれかを設定またはプロパティでは、以上の計算、それらのプロパティを保存する必要をオフにメッセージを変更されたとします。</span><span class="sxs-lookup"><span data-stu-id="22530-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="22530-123">プロパティがユーザーに表示する必要がありますが計算するためダイアログ ボックスが表示されません。</span><span class="sxs-lookup"><span data-stu-id="22530-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="22530-124">**InitNew**に渡される 1 つは別の作業中のメッセージ、サイトへの参照は、フォームに場合、は、使用できなくするために元のサイトをリリースします。</span><span class="sxs-lookup"><span data-stu-id="22530-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="22530-125">_PMessageSite_と_pMessage_パラメーターからは、サイトのメッセージとメッセージへのポインターを格納し、その参照カウントをインクリメントするのには、両方のオブジェクトの[IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="22530-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="22530-126">メッセージ クラスの適切な**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) と**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))、新しいメッセージのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="22530-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="22530-127">多くのメッセージ クラスは、新しいメッセージの**PR_MESSAGE_FLAGS**を MSGFLAG_UNSENT などの設定します。</span><span class="sxs-lookup"><span data-stu-id="22530-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="22530-128">戻る前にフォームにエラーがない場合は、[通常](normal-state.md)状態の遷移が発生しました。</span><span class="sxs-lookup"><span data-stu-id="22530-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="22530-129">[IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出すことによって登録されているすべてのビューアーに新着メッセージの通知を送信して、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="22530-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="22530-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="22530-130">Notes to callers</span></span>

<span data-ttu-id="22530-131">**InitNew**の呼び出しが成功したら、次の必要なプロパティおよびその他、フォームに設定されていることを引き受けることができます。</span><span class="sxs-lookup"><span data-stu-id="22530-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="22530-132">**PR_DELETE_AFTER_SUBMIT**([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22530-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="22530-133">**PR_IMPORTANCE**([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22530-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="22530-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED**([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22530-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="22530-135">**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22530-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="22530-136">**PR_READ_RECEIPT_REQUESTED**([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22530-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="22530-137">**PR_SENSITIVITY**([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22530-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="22530-138">**PR_SENTMAIL_ENTRYID**([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22530-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="22530-139">フォームの状態の詳細については、[フォームの状態](form-states.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="22530-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="22530-140">ストレージ ・ オブジェクトを初期化する方法の詳細については、 [IPersistStorage::InitNew](http://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx)メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="22530-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](http://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22530-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="22530-141">See also</span></span>



[<span data-ttu-id="22530-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22530-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

