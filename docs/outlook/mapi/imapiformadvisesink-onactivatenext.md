---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d647b41018afbade91dffb2818b48b0738148855
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411765"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="fca16-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="fca16-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="fca16-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fca16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fca16-105">表示する次のメッセージのメッセージ クラスをフォームで処理できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fca16-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="fca16-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fca16-106">Parameters</span></span>

 <span data-ttu-id="fca16-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="fca16-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="fca16-108">[in]次のメッセージのメッセージ クラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fca16-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="fca16-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="fca16-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="fca16-110">[in]次に表示するメッセージ **の PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされたクライアント定義フラグまたはプロバイダー定義フラグのビットマスクで、メッセージが含まれるコンテンツ テーブルに関する状態情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="fca16-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="fca16-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="fca16-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="fca16-112">[in]メッセージの現在の状態を示す次のメッセージの **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fca16-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="fca16-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="fca16-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="fca16-114">[out]新しいフォームが必要な場合に、新しいフォームに使用されるフォーム オブジェクトの [IPersistMessage](ipersistmessageiunknown.md) 実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fca16-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="fca16-115">現在のフォーム オブジェクトを使用して次のメッセージを表示および保存できる場合は、NULL へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="fca16-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fca16-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="fca16-116">Return value</span></span>

<span data-ttu-id="fca16-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="fca16-117">S_OK</span></span> 
  
> <span data-ttu-id="fca16-118">通知が成功し、フォームは次のメッセージを処理できます。</span><span class="sxs-lookup"><span data-stu-id="fca16-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="fca16-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="fca16-119">S_FALSE</span></span> 
  
> <span data-ttu-id="fca16-120">フォームは、次のメッセージのメッセージ クラスを処理します。</span><span class="sxs-lookup"><span data-stu-id="fca16-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fca16-121">注釈</span><span class="sxs-lookup"><span data-stu-id="fca16-121">Remarks</span></span>

<span data-ttu-id="fca16-122">フォーム ビューアーは **IMAPIFormAdviseSink::OnActivateNext** メソッドを呼び出して、フォルダー内に次のメッセージを表示できるかどうかをフォームが判断するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="fca16-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="fca16-123">次のメッセージは、任意のクラスのメッセージである可能性がありますが、通常は同じクラスまたは関連するクラスです。</span><span class="sxs-lookup"><span data-stu-id="fca16-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="fca16-124">これにより、クライアント アプリケーションが可能な限りフォーム オブジェクトを再利用することで、同じクラスの複数のメッセージを読み取るプロセスが効率的になります。</span><span class="sxs-lookup"><span data-stu-id="fca16-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="fca16-125">ほとんどのフォーム オブジェクトは  _、lpszMessageClass_ パラメーターが指すメッセージ クラスを使用して、次のメッセージを処理できるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="fca16-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="fca16-126">通常、フォームは、既定のクラスに属するメッセージに加えて、フォームの既定のクラスがサブクラスであるクラスに属するメッセージを処理できます。</span><span class="sxs-lookup"><span data-stu-id="fca16-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="fca16-127">ただし、フォームは他の要素を使用して、次のメッセージの送信済み状態や送信されていない状態など、メッセージを処理できるかどうかを疑問なく判断できます。</span><span class="sxs-lookup"><span data-stu-id="fca16-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fca16-128">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="fca16-128">Notes to implementers</span></span>

<span data-ttu-id="fca16-129">フォームS_OKメッセージ クラスを処理できる場合は  _、ppPersistMessage_ パラメーターの値と NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="fca16-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="fca16-130">フォームで処理できないメッセージを処理できる新しいフォームを作成できる場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="fca16-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="fca16-131">フォームのクラス ファクトリを呼び出して、新しいフォーム オブジェクトのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="fca16-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="fca16-132">そのインスタンスを  _ppPersistMessage_ ポインター パラメーターの内容に格納します。</span><span class="sxs-lookup"><span data-stu-id="fca16-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="fca16-133">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="fca16-133">Return S_OK.</span></span>
    
<span data-ttu-id="fca16-134">フォーム ビューアーは _、ppPersistMessage_ が指すオブジェクトに属する [IPersistMessage::Load](ipersistmessage-load.md)メソッドを使用してメッセージを読み込む。</span><span class="sxs-lookup"><span data-stu-id="fca16-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="fca16-135">作成できるフォームもフォームも次のメッセージを処理しない場合は、次のメッセージをS_FALSE。</span><span class="sxs-lookup"><span data-stu-id="fca16-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="fca16-136">ただし、フォーム ビューアーのパフォーマンスが低下する原因となるので、一般に、フォームはこの値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fca16-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fca16-137">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="fca16-137">MFCMAPI reference</span></span>

<span data-ttu-id="fca16-138">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fca16-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fca16-139">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="fca16-139">**File**</span></span>|<span data-ttu-id="fca16-140">**関数**</span><span class="sxs-lookup"><span data-stu-id="fca16-140">**Function**</span></span>|<span data-ttu-id="fca16-141">**コメント**</span><span class="sxs-lookup"><span data-stu-id="fca16-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fca16-142">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="fca16-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="fca16-143">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="fca16-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="fca16-144">MFCMAPI は **IMAPIFormAdviseSink::OnActivateNext** メソッドを使用して [IMAPIViewContext::ActivateNext メソッドを実装](imapiviewcontext-activatenext.md) します。</span><span class="sxs-lookup"><span data-stu-id="fca16-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fca16-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="fca16-145">See also</span></span>



[<span data-ttu-id="fca16-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="fca16-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="fca16-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fca16-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="fca16-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="fca16-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="fca16-149">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fca16-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="fca16-150">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fca16-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="fca16-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fca16-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


<span data-ttu-id="fca16-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="fca16-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

