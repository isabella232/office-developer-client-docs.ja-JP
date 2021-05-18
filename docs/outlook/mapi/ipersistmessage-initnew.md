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
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="36e46-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="36e46-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="36e46-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36e46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36e46-105">新しいメッセージを初期化します。</span><span class="sxs-lookup"><span data-stu-id="36e46-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="36e46-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="36e46-106">Parameters</span></span>

 <span data-ttu-id="36e46-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="36e46-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="36e46-108">[in]フォームがビューアーでメッセージを処理するために使用するメッセージ サイトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="36e46-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="36e46-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="36e46-109">_pMessage_</span></span>
  
> <span data-ttu-id="36e46-110">[in]新しいメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="36e46-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36e46-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="36e46-111">Return value</span></span>

<span data-ttu-id="36e46-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="36e46-112">S_OK</span></span> 
  
> <span data-ttu-id="36e46-113">新しいメッセージが正常に初期化されました。</span><span class="sxs-lookup"><span data-stu-id="36e46-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36e46-114">注釈</span><span class="sxs-lookup"><span data-stu-id="36e46-114">Remarks</span></span>

<span data-ttu-id="36e46-115">フォーム ビューアーは、ユーザーがフォームで処理するメッセージ クラスに属する新しいメッセージを書き込むときに **、IPersistMessage::InitNew** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="36e46-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="36e46-116">フォーム オブジェクトに有効なユーザー インターフェイス ポインターがある場合は、メッセージ オブジェクトのユーザー インターフェイスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="36e46-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="36e46-117">**InitNew** は、フォームが初期化されていない状態以外の状態にある場合 [は呼び出す必要](uninitialized-state.md) があります。</span><span class="sxs-lookup"><span data-stu-id="36e46-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="36e46-118">**InitNew** が呼び出された場合にフォームが他の状態の 1 つにある場合は、次のE_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="36e46-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="36e46-119">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="36e46-119">Notes to implementers</span></span>

<span data-ttu-id="36e46-120">通常、保存されていないプロパティを持つメッセージは変更済みとしてマークされ、クライアントは、これらのプロパティを保存するかどうかをユーザーに求めるダイアログ ボックスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="36e46-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="36e46-121">ユーザーがメッセージを保存する必要がある場合は、データを保存し、メッセージをクリーンとしてマークし、正常に終了します。</span><span class="sxs-lookup"><span data-stu-id="36e46-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="36e46-122">ただし、新しく初期化されたメッセージの処理に 1 つ以上の計算プロパティの設定が含まれる場合、それらのプロパティを保存することが重要である場合は、メッセージを変更済みとしてマークしません。</span><span class="sxs-lookup"><span data-stu-id="36e46-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="36e46-123">計算されたプロパティはユーザーには表示されない必要があります。ダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="36e46-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="36e46-124">フォームに **InitNew** に渡されるメッセージ サイト以外のアクティブなメッセージ サイトへの参照がある場合は、元のサイトが使用されなくなったため、元のサイトを解放します。</span><span class="sxs-lookup"><span data-stu-id="36e46-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="36e46-125">_pMessageSite_ パラメーターと _pMessage_ パラメーターからメッセージ サイトへのポインターとメッセージを格納し、両方のオブジェクトの [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出して、参照カウントを増やします。</span><span class="sxs-lookup"><span data-stu-id="36e46-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="36e46-126">新しいメッセージ **の** PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティと **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティを、メッセージ クラスに適した値に設定します。</span><span class="sxs-lookup"><span data-stu-id="36e46-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="36e46-127">たとえば、多くのメッセージ クラスは、新しい **PR_MESSAGE_FLAGS** のMSGFLAG_UNSENTに設定します。</span><span class="sxs-lookup"><span data-stu-id="36e46-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="36e46-128">返す前に、エラーが発生したことがない場合は、フォームを [Normal](normal-state.md) 状態に移行します。</span><span class="sxs-lookup"><span data-stu-id="36e46-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="36e46-129">[IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出して、登録されているすべての閲覧者に新しいメッセージ通知を送信し、S_OK。</span><span class="sxs-lookup"><span data-stu-id="36e46-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="36e46-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="36e46-130">Notes to callers</span></span>

<span data-ttu-id="36e46-131">**InitNew** を正常に呼び出した後、フォームに対して次の必須プロパティと他のプロパティが設定されていないと仮定できます。</span><span class="sxs-lookup"><span data-stu-id="36e46-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="36e46-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36e46-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="36e46-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36e46-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="36e46-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36e46-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="36e46-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36e46-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="36e46-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36e46-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="36e46-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36e46-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="36e46-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36e46-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="36e46-139">フォームの状態の詳細については、「フォームの状態」 [を参照してください](form-states.md)。</span><span class="sxs-lookup"><span data-stu-id="36e46-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="36e46-140">記憶域オブジェクトの初期化方法の詳細については [、「IPersistStorage::InitNew メソッド」を参照](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) してください。</span><span class="sxs-lookup"><span data-stu-id="36e46-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="36e46-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="36e46-141">See also</span></span>



[<span data-ttu-id="36e46-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36e46-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

