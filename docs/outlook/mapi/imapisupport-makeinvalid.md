---
title: imapisupportmakeinvalid
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 84e87f8a8d3c419afc4b86e200aeaba57e6a85f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427494"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="4c283-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="4c283-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="4c283-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c283-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c283-105">オブジェクトを使用不可としてマークします。</span><span class="sxs-lookup"><span data-stu-id="4c283-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="4c283-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4c283-106">Parameters</span></span>

 <span data-ttu-id="4c283-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4c283-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4c283-108">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c283-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4c283-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="4c283-109">_lpObject_</span></span>
  
> <span data-ttu-id="4c283-110">順番無効化されるオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4c283-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="4c283-111">オブジェクトのインターフェイスは、 **IUnknown**から派生している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c283-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="4c283-112">_ulrefcount_</span><span class="sxs-lookup"><span data-stu-id="4c283-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="4c283-113">順番オブジェクトの現在の参照カウント。</span><span class="sxs-lookup"><span data-stu-id="4c283-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="4c283-114">_cmethods_</span><span class="sxs-lookup"><span data-stu-id="4c283-114">_cMethods_</span></span>
  
> <span data-ttu-id="4c283-115">順番オブジェクトの vtable 内のメソッドの数。</span><span class="sxs-lookup"><span data-stu-id="4c283-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c283-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="4c283-116">Return value</span></span>

<span data-ttu-id="4c283-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c283-117">S_OK</span></span> 
  
> <span data-ttu-id="4c283-118">オブジェクトが正常に使用できないとマークされました。</span><span class="sxs-lookup"><span data-stu-id="4c283-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c283-119">注釈</span><span class="sxs-lookup"><span data-stu-id="4c283-119">Remarks</span></span>

<span data-ttu-id="4c283-120">**imapisupport:: makeinvalid**メソッドは、すべてのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="4c283-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="4c283-121">無効化するオブジェクトは、 **iunknown**インターフェイスまたは**iunknown**から派生したインターフェイスから派生している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c283-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="4c283-122">**makeinvalid**は、オブジェクトの vtable を、 **iunknown:: AddRef**メソッドと**iunknown:: Release**メソッドが期待どおりに実行するのと同じようなサイズのスタブ vtable で置き換えることにより、オブジェクトを使用不能としてマークします。</span><span class="sxs-lookup"><span data-stu-id="4c283-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="4c283-123">ただし、その他のメソッドは失敗し、値 MAPI_E_INVALID_OBJECT が返されます。</span><span class="sxs-lookup"><span data-stu-id="4c283-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4c283-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4c283-124">Notes to callers</span></span>

<span data-ttu-id="4c283-125">サービスプロバイダーとメッセージサービスは、通常、シャットダウン時に**makeinvalid**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4c283-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="4c283-126">ただし、 **makeinvalid**はいつでも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="4c283-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="4c283-127">たとえば、クライアントがオブジェクトを解放せずにそのサブオブジェクトの一部を解放しない場合は、直ちに**makeinvalid**を呼び出すことで、それらのサブオブジェクトを解放できます。</span><span class="sxs-lookup"><span data-stu-id="4c283-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="4c283-128">無効にしようとしているオブジェクトを所有している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c283-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="4c283-129">少なくとも16バイトの長さで、vtable に少なくとも3つのメソッドが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c283-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="4c283-130">**makeinvalid**を呼び出してから、関連付けられたデータ構造を破棄するなど、通常はオブジェクトのリリース時に実行されるすべてのシャットダウン作業を実行できます。</span><span class="sxs-lookup"><span data-stu-id="4c283-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="4c283-131">MAPI は[MAPIFreeBuffer](mapifreebuffer.md)を呼び出してメモリを解放し、その後オブジェクトを解放するため、オブジェクトをサポートするコードをメモリに保持する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4c283-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="4c283-132">リソースを解放し、 **makeinvalid**を呼び出し、無効化されたオブジェクトを無視することができます。</span><span class="sxs-lookup"><span data-stu-id="4c283-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c283-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="4c283-133">See also</span></span>



[<span data-ttu-id="4c283-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="4c283-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="4c283-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c283-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

