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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3ce4d57ab4837f40ffbc898fde68e44cc802676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800504"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="b2ecb-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="b2ecb-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="b2ecb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2ecb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2ecb-105">フォームを表示するのには、次のメッセージのメッセージ クラスを処理できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="b2ecb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b2ecb-106">Parameters</span></span>

 <span data-ttu-id="b2ecb-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="b2ecb-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="b2ecb-108">[in]次のメッセージのメッセージ クラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="b2ecb-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="b2ecb-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="b2ecb-110">[in]メッセージが含まれているコンテンツのテーブルに関するステータス情報を提供する、 **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティを表示するには、次のメッセージからコピーされた、クライアントが定義されているか、プロバイダーで定義されているフラグのビットマスクします。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="b2ecb-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="b2ecb-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="b2ecb-112">[in]フラグは、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティを表示するのには、次のメッセージからコピーのビットマップへのポインターでは、メッセージの現在の状態を示します。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="b2ecb-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="b2ecb-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="b2ecb-114">[out][IPersistMessage](ipersistmessageiunknown.md)の実装の新しいフォームで、新しいフォームが必要な場合に使用されるフォーム オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="b2ecb-115">表示し、次のメッセージを保存する、現在のフォームを使用できる場合、NULL へのポインターを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b2ecb-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b2ecb-116">Return value</span></span>

<span data-ttu-id="b2ecb-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2ecb-117">S_OK</span></span> 
  
> <span data-ttu-id="b2ecb-118">通知が成功し、フォームは、次のメッセージを処理できます。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="b2ecb-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b2ecb-119">S_FALSE</span></span> 
  
> <span data-ttu-id="b2ecb-120">フォームでは、次のメッセージのメッセージ クラスは処理されません。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2ecb-121">備考</span><span class="sxs-lookup"><span data-stu-id="b2ecb-121">Remarks</span></span>

<span data-ttu-id="b2ecb-122">フォームの閲覧者は、フォルダー内の次のメッセージを表示できるかどうかを決定するフォームのために**IMAPIFormAdviseSink::OnActivateNext**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="b2ecb-123">次のメッセージは、任意のクラスのメッセージである可能性がありますが、通常同じクラスの関連するクラスです。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="b2ecb-124">こうと、可能な場合、フォーム オブジェクトを再利用するクライアント アプリケーションを有効にするとより効率的な同じクラスの複数のメッセージを読み取って処理します。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="b2ecb-125">フォームのほとんどのオブジェクトは次のメッセージを処理できるかどうかを判断するのには、 _lpszMessageClass_パラメーターで指定されたメッセージ クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="b2ecb-126">通常、フォームは、フォームの既定のクラスが既定のクラスに属しているメッセージだけでなく、サブクラスがクラスに属しているメッセージを処理できます。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="b2ecb-127">ただし、フォームでは、質問しないかどうか、メッセージの処理、次のメッセージの送信または未送信の状態などを決定するのにその他の要因を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b2ecb-128">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="b2ecb-128">Notes to implementers</span></span>

<span data-ttu-id="b2ecb-129">フォームは、メッセージ クラスを処理できる場合、 _ppPersistMessage_パラメーターに S_OK と NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="b2ecb-130">フォームは、フォームが処理することがあるメッセージを処理できる新しいフォームを作成できます、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="b2ecb-131">新しいフォーム オブジェクトのインスタンスを作成するのには、フォームのクラス ファクトリを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="b2ecb-132">_PpPersistMessage_ポインター パラメーターの内容でそのインスタンスを格納します。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="b2ecb-133">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="b2ecb-133">Return S_OK.</span></span>
    
<span data-ttu-id="b2ecb-134">フォーム ビューアーは、メッセージを_ppPersistMessage_が指すオブジェクトが所属する[IPersistMessage::Load](ipersistmessage-load.md)メソッドを使用して読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="b2ecb-135">フォームも作成できるフォームには、次のメッセージが処理される場合は、S_FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="b2ecb-136">ただし、一般に、フォームを返さないでくださいこの値に発生するためは、フォームのビューアーでのパフォーマンスを低下します。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b2ecb-137">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="b2ecb-137">MFCMAPI reference</span></span>

<span data-ttu-id="b2ecb-138">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="b2ecb-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b2ecb-139">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="b2ecb-139">**File**</span></span>|<span data-ttu-id="b2ecb-140">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="b2ecb-140">**Function**</span></span>|<span data-ttu-id="b2ecb-141">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="b2ecb-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b2ecb-142">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b2ecb-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b2ecb-143">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="b2ecb-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="b2ecb-144">MFCMAPI では、 **IMAPIFormAdviseSink::OnActivateNext**メソッドを使用して、 [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="b2ecb-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2ecb-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="b2ecb-145">See also</span></span>



[<span data-ttu-id="b2ecb-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="b2ecb-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="b2ecb-147">IPersistMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2ecb-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="b2ecb-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="b2ecb-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="b2ecb-149">PidTagMessageFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b2ecb-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="b2ecb-150">PidTagMessageStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b2ecb-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="b2ecb-151">IMAPIFormAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2ecb-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


<span data-ttu-id="b2ecb-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b2ecb-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

