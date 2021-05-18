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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7200e7d226eb148fef094ab8540990644d2d4c99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316588"
---
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="e9597-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="e9597-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="e9597-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9597-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9597-105">ストリームにアクセスするストレージ オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="e9597-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="e9597-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9597-106">Parameters</span></span>

 <span data-ttu-id="e9597-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="e9597-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="e9597-108">[in]ストリーム オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e9597-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="e9597-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e9597-109">_lpInterface_</span></span>
  
> <span data-ttu-id="e9597-110">[in]  _lpUnkIn_ が指すストリームにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e9597-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="e9597-111">次の値は有効です:IID_IStream、IID_ILockBytes、または **null** は [、IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) インターフェイスを使用してストリームにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9597-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="e9597-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e9597-112">_ulFlags_</span></span>
  
> <span data-ttu-id="e9597-113">[in]ストリーム オブジェクトを基準にストレージ オブジェクトを作成する方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e9597-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="e9597-114">既定では、ストレージは読み取り専用アクセスで作成され、ストリームは記憶域の位置 0 から始まります。</span><span class="sxs-lookup"><span data-stu-id="e9597-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="e9597-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e9597-115">The following flags can be set:</span></span>
    
<span data-ttu-id="e9597-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="e9597-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="e9597-117">ストリーム オブジェクト用に新しいストレージ オブジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9597-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="e9597-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="e9597-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="e9597-119">記憶域オブジェクトは、ストリームの現在の位置から開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9597-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="e9597-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="e9597-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="e9597-121">呼び出し元は、返されるストレージ オブジェクトに対する読み取り/書き込みアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9597-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="e9597-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="e9597-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="e9597-123">記憶域オブジェクトは、位置 0 から始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9597-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="e9597-124">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="e9597-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="e9597-125">[out]記憶域オブジェクトへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="e9597-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e9597-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9597-126">Return value</span></span>

<span data-ttu-id="e9597-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9597-127">S_OK</span></span> 
  
> <span data-ttu-id="e9597-128">記憶域オブジェクトが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="e9597-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9597-129">注釈</span><span class="sxs-lookup"><span data-stu-id="e9597-129">Remarks</span></span>

<span data-ttu-id="e9597-130">**IMAPISupport::IStorageFromStream** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="e9597-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="e9597-131">サービス プロバイダーは **、IStorageFromStream** を呼び出して、特定のプロパティを開く際に使用するストレージ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="e9597-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="e9597-132">[IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx)インターフェイスの独自の実装を持つサービス プロバイダーは **、IStorageFromStream を呼び出す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="e9597-132">Service providers that have their own implementation of the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="e9597-133">**IStorageFromStream** によって作成されたストレージ オブジェクトは、ストリームの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出して、その参照カウントをインクリメントし、ストレージが解放されるとカウントをデクリメントします。</span><span class="sxs-lookup"><span data-stu-id="e9597-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e9597-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e9597-134">Notes to callers</span></span>

<span data-ttu-id="e9597-135">オブジェクトの [1 つの IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドが呼び出され **、IStorage** インターフェイスでプロパティを開く場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="e9597-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="e9597-136">プロパティの読み取り/書き込みアクセス許可を持つストリーム オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="e9597-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="e9597-137">プロパティ ストリームを内部的にストレージ オブジェクトとしてマークします。</span><span class="sxs-lookup"><span data-stu-id="e9597-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="e9597-138">**IStorageFromStream を呼び出して**、ストレージ オブジェクトを生成します。</span><span class="sxs-lookup"><span data-stu-id="e9597-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="e9597-139">このストレージ オブジェクトへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="e9597-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="e9597-140">ストレージ オブジェクトを使用する追加のインターフェイスを実装する場合は、ストレージ オブジェクトをラップするオブジェクトを作成し、より高い [レベルの IUnknown::QueryInterface メソッドを実装](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) します。</span><span class="sxs-lookup"><span data-stu-id="e9597-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="e9597-141">IStorage を使用して作成された **場合は、IStream** インターフェイスでプロパティ **を開かれません**。</span><span class="sxs-lookup"><span data-stu-id="e9597-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="e9597-142">逆に、IStream を使用して作成した **場合は、IStorage** インターフェイスでプロパティを **開かれません**。</span><span class="sxs-lookup"><span data-stu-id="e9597-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="e9597-143">1 つの例外を除き **、IStreamDocfile** インターフェイスを使用してコンテナー間でストレージ オブジェクトをストリームすることもできますが、IID_IStreamDocfile インターフェイス識別子は **OpenProperty** メソッドの  _lpInterface_ パラメーターで渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9597-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9597-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9597-144">See also</span></span>



[<span data-ttu-id="e9597-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="e9597-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="e9597-146">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9597-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

