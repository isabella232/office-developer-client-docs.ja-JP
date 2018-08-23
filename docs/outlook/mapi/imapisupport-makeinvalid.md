---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 75771670f58f4cd65e15a02d08e6f78ab9d71755
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570738"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="874a7-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="874a7-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="874a7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="874a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="874a7-105">オブジェクトを使用不可としてマークを付けます。</span><span class="sxs-lookup"><span data-stu-id="874a7-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="874a7-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="874a7-106">Parameters</span></span>

 <span data-ttu-id="874a7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="874a7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="874a7-108">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="874a7-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="874a7-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="874a7-109">_lpObject_</span></span>
  
> <span data-ttu-id="874a7-110">[in]無効化するオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="874a7-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="874a7-111">オブジェクトのインターフェイスは、 **IUnknown**から派生する必要があります。</span><span class="sxs-lookup"><span data-stu-id="874a7-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="874a7-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="874a7-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="874a7-113">[in]オブジェクトの現在の参照カウント。</span><span class="sxs-lookup"><span data-stu-id="874a7-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="874a7-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="874a7-114">_cMethods_</span></span>
  
> <span data-ttu-id="874a7-115">[in]オブジェクトの vtable 内のメソッドの数。</span><span class="sxs-lookup"><span data-stu-id="874a7-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="874a7-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="874a7-116">Return value</span></span>

<span data-ttu-id="874a7-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="874a7-117">S_OK</span></span> 
  
> <span data-ttu-id="874a7-118">オブジェクトは、使用不可が正しく設定されました。</span><span class="sxs-lookup"><span data-stu-id="874a7-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="874a7-119">注釈</span><span class="sxs-lookup"><span data-stu-id="874a7-119">Remarks</span></span>

<span data-ttu-id="874a7-120">サポートのすべてのオブジェクトの**IMAPISupport::MakeInvalid**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="874a7-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="874a7-121">オブジェクトが無効になりますは、 **IUnknown**インターフェイスから、または**IUnknown**から派生したインターフェイスから派生する必要があります。</span><span class="sxs-lookup"><span data-stu-id="874a7-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="874a7-122">**MakeInvalid**は、スタブのようなサイズが、 **IUnknown::AddRef**と**リ ス**のメソッドが期待どおりの vtable が同じオブジェクトの vtable に置き換えることによって使用不可としてオブジェクトをマークします。</span><span class="sxs-lookup"><span data-stu-id="874a7-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="874a7-123">ただし、他のすべてのメソッドが失敗する、MAPI_E_INVALID_OBJECT の値を返します。</span><span class="sxs-lookup"><span data-stu-id="874a7-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="874a7-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="874a7-124">Notes to callers</span></span>

<span data-ttu-id="874a7-125">サービス プロバイダーとサービスのメッセージは通常のシャット ダウン時に**MakeInvalid**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="874a7-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="874a7-126">ただし、 **MakeInvalid**は、いつでも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="874a7-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="874a7-127">などのクライアントは、その下位オブジェクトのいくつかのボタンを押したままオブジェクトを解放する場合、は、これらの下位オブジェクトを解放するには、すぐに**MakeInvalid**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="874a7-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="874a7-128">無効にしようとするオブジェクトを所有する必要があります。</span><span class="sxs-lookup"><span data-stu-id="874a7-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="874a7-129">16 バイト長と、その vtable の少なくとも 3 つの方法があること必要があります。</span><span class="sxs-lookup"><span data-stu-id="874a7-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="874a7-130">**MakeInvalid**を呼び出すし、シャット ダウンなどの作業、関連するデータ構造を破棄するオブジェクトのリリース中に通常行われるを実行できます。</span><span class="sxs-lookup"><span data-stu-id="874a7-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="874a7-131">MAPI が[MAPIFreeBuffer](mapifreebuffer.md)を呼び出すことによってメモリを解放して、オブジェクトを解放するため、オブジェクトをサポートするためにコードをメモリに保存されない必要があります。</span><span class="sxs-lookup"><span data-stu-id="874a7-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="874a7-132">リソースを解放し、 **MakeInvalid**を呼び出すし、無効化されたオブジェクトを無視できます。</span><span class="sxs-lookup"><span data-stu-id="874a7-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="874a7-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="874a7-133">See also</span></span>



[<span data-ttu-id="874a7-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="874a7-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="874a7-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="874a7-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

