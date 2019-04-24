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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d647b41018afbade91dffb2818b48b0738148855
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329436"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="29031-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="29031-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="29031-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29031-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29031-105">フォームが次に表示されるメッセージのメッセージクラスを処理できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="29031-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="29031-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="29031-106">Parameters</span></span>

 <span data-ttu-id="29031-107">_lpszmessageclass_</span><span class="sxs-lookup"><span data-stu-id="29031-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="29031-108">順番次のメッセージのメッセージクラスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="29031-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="29031-109">_ulmessagestatus_</span><span class="sxs-lookup"><span data-stu-id="29031-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="29031-110">順番メッセージが含まれる contents テーブルに関する状態情報を提供する、クライアント定義またはプロバイダー定義のフラグのビットマスク。これは、表示する次のメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされます。順番.</span><span class="sxs-lookup"><span data-stu-id="29031-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="29031-111">_ulmessageflags_</span><span class="sxs-lookup"><span data-stu-id="29031-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="29031-112">順番メッセージの現在の状態を示す次のメッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="29031-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="29031-113">_pppersistmessage_</span><span class="sxs-lookup"><span data-stu-id="29031-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="29031-114">読み上げ新しいフォームが必要な場合は、新しいフォームに使用される form オブジェクトの[IPersistMessage](ipersistmessageiunknown.md)実装へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="29031-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="29031-115">現在の form オブジェクトを使用して次のメッセージを表示し保存できる場合は、NULL へのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="29031-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="29031-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="29031-116">Return value</span></span>

<span data-ttu-id="29031-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="29031-117">S_OK</span></span> 
  
> <span data-ttu-id="29031-118">通知は正常に実行され、フォームは次のメッセージを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="29031-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="29031-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="29031-119">S_FALSE</span></span> 
  
> <span data-ttu-id="29031-120">フォームでは、次のメッセージのメッセージクラスは処理されません。</span><span class="sxs-lookup"><span data-stu-id="29031-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="29031-121">解説</span><span class="sxs-lookup"><span data-stu-id="29031-121">Remarks</span></span>

<span data-ttu-id="29031-122">フォームビューアーは、 **IMAPIFormAdviseSink:: OnActivateNext**メソッドを呼び出して、フォームが次のメッセージをフォルダー内に表示できるかどうかを判断できるようにします。</span><span class="sxs-lookup"><span data-stu-id="29031-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="29031-123">次のメッセージは任意のクラスのメッセージである可能性がありますが、通常は同じクラスまたは関連クラスのものです。</span><span class="sxs-lookup"><span data-stu-id="29031-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="29031-124">これにより、クライアントアプリケーションが可能な限りフォームオブジェクトを再利用できるようにすることで、同じクラスの複数のメッセージをより効率的に読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="29031-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="29031-125">ほとんどの form オブジェクトは、 _lpszmessageclass_パラメーターで指定されたメッセージクラスを使用して、次のメッセージを処理できるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="29031-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="29031-126">通常、フォームは、既定のクラスに属するメッセージに加えて、フォームの既定のクラスがサブクラスであるクラスに属するメッセージを処理できます。</span><span class="sxs-lookup"><span data-stu-id="29031-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="29031-127">ただし、フォームで他の要素を使用して、メッセージを処理できるかどうか (次のメッセージの送信済みまたは未送信の状態など) を確認することはできません。</span><span class="sxs-lookup"><span data-stu-id="29031-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="29031-128">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="29031-128">Notes to implementers</span></span>

<span data-ttu-id="29031-129">フォームがメッセージクラスを処理できる場合は、 _pppersistmessage_パラメーターで S_OK および NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="29031-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="29031-130">フォームで処理できないメッセージを処理できる新しいフォームを作成できる場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="29031-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="29031-131">フォームのクラスファクトリを呼び出して、新しい form オブジェクトのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="29031-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="29031-132">そのインスタンスを_pppersistmessage_ポインターパラメーターの内容に格納します。</span><span class="sxs-lookup"><span data-stu-id="29031-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="29031-133">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="29031-133">Return S_OK.</span></span>
    
<span data-ttu-id="29031-134">フォームビューアーは、 _pppersistmessage_が指すオブジェクトに属する[IPersistMessage:: load](ipersistmessage-load.md)メソッドを使用して、メッセージを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="29031-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="29031-135">作成できるフォームまたはフォームのいずれも、次のメッセージを処理できる場合は、S_FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="29031-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="29031-136">ただし、一般に、フォームビューアーのパフォーマンスが低下する原因となるため、フォームはこの値を返さないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="29031-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="29031-137">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="29031-137">MFCMAPI reference</span></span>

<span data-ttu-id="29031-138">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29031-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="29031-139">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="29031-139">**File**</span></span>|<span data-ttu-id="29031-140">**関数**</span><span class="sxs-lookup"><span data-stu-id="29031-140">**Function**</span></span>|<span data-ttu-id="29031-141">**コメント**</span><span class="sxs-lookup"><span data-stu-id="29031-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="29031-142">MAPIFormFunctions</span><span class="sxs-lookup"><span data-stu-id="29031-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="29031-143">cmymapiformviewer:: ActivateNext</span><span class="sxs-lookup"><span data-stu-id="29031-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="29031-144">mfcmapi は、 **IMAPIFormAdviseSink:: OnActivateNext**メソッドを使用して、 [imapiviewcontext:: ActivateNext](imapiviewcontext-activatenext.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="29031-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="29031-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="29031-145">See also</span></span>



[<span data-ttu-id="29031-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="29031-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="29031-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="29031-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="29031-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="29031-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="29031-149">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="29031-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="29031-150">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="29031-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="29031-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="29031-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


<span data-ttu-id="29031-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="29031-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

