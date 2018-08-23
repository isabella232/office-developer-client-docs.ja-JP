---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a73c87f172b4c97379bb9cd117679d3947c188af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800753"
---
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="947eb-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="947eb-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="947eb-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="947eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="947eb-105">ストリームにアクセスするためのストレージ オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="947eb-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="947eb-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="947eb-106">Parameters</span></span>

 <span data-ttu-id="947eb-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="947eb-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="947eb-108">[in]ストリーム オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="947eb-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="947eb-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="947eb-109">_lpInterface_</span></span>
  
> <span data-ttu-id="947eb-110">[in]_LpUnkIn_で指定されたストリームにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="947eb-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="947eb-111">次の値のいずれかが無効です: IID_IStream、IID_ILockBytes、または**null**ストリームにアクセスするのには、 [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)インターフェイスを使用することを示します。</span><span class="sxs-lookup"><span data-stu-id="947eb-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="947eb-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="947eb-112">_ulFlags_</span></span>
  
> <span data-ttu-id="947eb-113">[in]記憶域オブジェクトのストリーム オブジェクトを作成する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="947eb-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="947eb-114">既定では、読み取り専用アクセス権を持つストレージを作成し、ストリームは、ストレージ内の位置 0 から始まりです。</span><span class="sxs-lookup"><span data-stu-id="947eb-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="947eb-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="947eb-115">The following flags can be set:</span></span>
    
<span data-ttu-id="947eb-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="947eb-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="947eb-117">新しいストレージ オブジェクトは、ストリーム オブジェクトを作成してください。</span><span class="sxs-lookup"><span data-stu-id="947eb-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="947eb-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="947eb-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="947eb-119">ストレージ オブジェクト、ストリームの現在位置で開始します。</span><span class="sxs-lookup"><span data-stu-id="947eb-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="947eb-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="947eb-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="947eb-121">呼び出し元に返された記憶域オブジェクトの読み取り/書き込み権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="947eb-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="947eb-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="947eb-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="947eb-123">ストレージ オブジェクトは、位置 0 で開始します。</span><span class="sxs-lookup"><span data-stu-id="947eb-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="947eb-124">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="947eb-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="947eb-125">[out]ストレージ オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="947eb-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="947eb-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="947eb-126">Return value</span></span>

<span data-ttu-id="947eb-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="947eb-127">S_OK</span></span> 
  
> <span data-ttu-id="947eb-128">ストレージ オブジェクトは正しく作成されました。</span><span class="sxs-lookup"><span data-stu-id="947eb-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="947eb-129">注釈</span><span class="sxs-lookup"><span data-stu-id="947eb-129">Remarks</span></span>

<span data-ttu-id="947eb-130">サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::IStorageFromStream**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="947eb-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="947eb-131">サービス プロバイダーは、特定のプロパティを開くときに使用するストレージ オブジェクトを作成するのには**IStorageFromStream**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="947eb-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="947eb-132">[IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx)インターフェイスの独自の実装を持つサービス ・ プロバイダーは、 **IStorageFromStream**を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="947eb-132">Service providers that have their own implementation of the [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="947eb-133">**IStorageFromStream**によって作成されたストレージ オブジェクトは、ストレージが解放されるときにストリームの[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)のメソッドの参照カウントと、デクリメントをインクリメントするにカウントを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="947eb-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="947eb-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="947eb-134">Notes to callers</span></span>

<span data-ttu-id="947eb-135">**IStorage**インターフェイスを使用してプロパティを開き、オブジェクトの 1 つの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドが呼び出されると、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="947eb-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="947eb-136">プロパティの読み取り/書き込み権限を持つ stream オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="947eb-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="947eb-137">プロパティ ストリームをストレージ オブジェクトとして内部的にマークします。</span><span class="sxs-lookup"><span data-stu-id="947eb-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="947eb-138">ストレージ ・ オブジェクトを生成するのには**IStorageFromStream**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="947eb-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="947eb-139">このストレージ オブジェクトへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="947eb-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="947eb-140">ストレージ オブジェクトを使用する追加のインターフェイスを実装する場合、ストレージ オブジェクトをラップするオブジェクトを作成しより高いレベルの[IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="947eb-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="947eb-141">**IStorage**で作成された場合は、 **IStream**インターフェイスを使用して開かれるプロパティを許可しません。</span><span class="sxs-lookup"><span data-stu-id="947eb-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="947eb-142">逆に、 **IStorage**インターフェイスを使用して開く**IStream**で作成されたプロパティを許可しません。</span><span class="sxs-lookup"><span data-stu-id="947eb-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="947eb-143">1 つの例外を除き、 **IStreamDocfile**インターフェイスを使用して、1 つのコンテナーから別のストレージ オブジェクトをストリーム配信してもかまいませんが、メソッドでは、 **OpenProperty**の _、IID_IStreamDocfile のインタ フェース識別子を渡す必要があります lpInterface_パラメーター。</span><span class="sxs-lookup"><span data-stu-id="947eb-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="947eb-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="947eb-144">See also</span></span>



[<span data-ttu-id="947eb-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="947eb-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="947eb-146">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="947eb-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

