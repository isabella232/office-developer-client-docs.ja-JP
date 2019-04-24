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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317151"
---
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="8d319-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="8d319-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="8d319-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d319-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d319-105">新しいメッセージを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8d319-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="8d319-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8d319-106">Parameters</span></span>

 <span data-ttu-id="8d319-107">_pメッセージ ite_</span><span class="sxs-lookup"><span data-stu-id="8d319-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="8d319-108">順番フォームがビューアー内のメッセージを操作するために使用するメッセージサイトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8d319-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="8d319-109">_pmessage_</span><span class="sxs-lookup"><span data-stu-id="8d319-109">_pMessage_</span></span>
  
> <span data-ttu-id="8d319-110">順番新しいメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8d319-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d319-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="8d319-111">Return value</span></span>

<span data-ttu-id="8d319-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d319-112">S_OK</span></span> 
  
> <span data-ttu-id="8d319-113">新しいメッセージが正常に初期化されました。</span><span class="sxs-lookup"><span data-stu-id="8d319-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d319-114">解説</span><span class="sxs-lookup"><span data-stu-id="8d319-114">Remarks</span></span>

<span data-ttu-id="8d319-115">フォームビューアーは、フォームが処理するメッセージクラスに属する新しいメッセージをユーザーが書き込むときに、 **IPersistMessage:: InitNew**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8d319-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="8d319-116">form オブジェクトに有効なユーザーインターフェイスポインターがある場合は、そのメッセージオブジェクトのユーザーインターフェイスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8d319-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="8d319-117">フォームが[初期化](uninitialized-state.md)されていない状態以外の状態にある場合は、 **InitNew**を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="8d319-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="8d319-118">**InitNew**が呼び出されたときに、フォームが他の状態のいずれかになっている場合は、E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="8d319-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8d319-119">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="8d319-119">Notes to implementers</span></span>

<span data-ttu-id="8d319-120">通常、保存されていないプロパティを持つメッセージは変更済みとしてマークされるため、クライアントは、これらのプロパティを保存するかどうかを確認するダイアログボックスを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="8d319-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="8d319-121">ユーザーがメッセージを保存することを示している場合は、データを保存し、メッセージを [クリーン] としてマークし、通常どおりに終了します。</span><span class="sxs-lookup"><span data-stu-id="8d319-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="8d319-122">ただし、新しく初期化されたメッセージを処理する場合は、1つ以上の計算プロパティを設定する必要があります。これらのプロパティを保存する場合は、メッセージを変更済みとしてマークしないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="8d319-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="8d319-123">ユーザーは、計算されたプロパティを非表示にする必要があるので、ダイアログボックスを表示する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8d319-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="8d319-124">フォームに、 **InitNew**に渡されたものとは異なるアクティブなメッセージサイトへの参照がある場合は、そのサイトが使用されなくなっているため、元のサイトを解放します。</span><span class="sxs-lookup"><span data-stu-id="8d319-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="8d319-125">メッセージサイトおよびメッセージへのポインターを pメッセージパラメーター __ と_pmessage_パラメーターから格納し、両方のオブジェクト ' [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出して参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="8d319-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="8d319-126">新しいメッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) および**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティを、自分のメッセージクラスに適したものに設定します。</span><span class="sxs-lookup"><span data-stu-id="8d319-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="8d319-127">多くのメッセージクラスでは、たとえば、新しいメッセージの**PR_MESSAGE_FLAGS**を MSGFLAG_UNSENT に設定します。</span><span class="sxs-lookup"><span data-stu-id="8d319-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="8d319-128">戻る前に、エラーが発生していない場合は、フォームを[通常](normal-state.md)の状態に移行します。</span><span class="sxs-lookup"><span data-stu-id="8d319-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="8d319-129">登録されているすべてのビューアーに新しいメッセージ通知を送信するには、 [IMAPIViewAdviseSink:: onnewmessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出し、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="8d319-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8d319-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="8d319-130">Notes to callers</span></span>

<span data-ttu-id="8d319-131">**InitNew**を正常に呼び出した後、フォームに対して次の必要なプロパティが設定されていると仮定できます。</span><span class="sxs-lookup"><span data-stu-id="8d319-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="8d319-132">**PR_DELETE_AFTER_SUBMIT**([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d319-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="8d319-133">**PR_IMPORTANCE**([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d319-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="8d319-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED**([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d319-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="8d319-135">**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d319-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="8d319-136">**PR_READ_RECEIPT_REQUESTED**([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d319-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="8d319-137">**PR_SENSITIVITY**([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d319-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="8d319-138">**PR_SENTMAIL_ENTRYID**([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d319-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="8d319-139">フォームの状態の詳細については、「[フォームの状態](form-states.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d319-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="8d319-140">ストレージオブジェクトが初期化される方法の詳細については、 [IPersistStorage:: InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx)メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d319-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d319-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d319-141">See also</span></span>



[<span data-ttu-id="8d319-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d319-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

