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
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="73679-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="73679-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="73679-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73679-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73679-105">stream にアクセスするためのストレージオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="73679-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="73679-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="73679-106">Parameters</span></span>

 <span data-ttu-id="73679-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="73679-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="73679-108">順番stream オブジェクトへのポインターを示します。</span><span class="sxs-lookup"><span data-stu-id="73679-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="73679-109">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="73679-109">_lpInterface_</span></span>
  
> <span data-ttu-id="73679-110">順番_lpUnkIn_によって参照されるストリームへのアクセスに使用されるインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="73679-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="73679-111">次のいずれかの値が有効です: IID_IStream、IID_ILockBytes、または**null**。これは、このストリームにアクセスするために[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスを使用する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="73679-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="73679-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="73679-112">_ulFlags_</span></span>
  
> <span data-ttu-id="73679-113">順番stream オブジェクトを基準にして、ストレージオブジェクトを作成する方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="73679-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="73679-114">既定では、記憶域は読み取り専用アクセスで作成され、ストリームの位置0から開始します。</span><span class="sxs-lookup"><span data-stu-id="73679-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="73679-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="73679-115">The following flags can be set:</span></span>
    
<span data-ttu-id="73679-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="73679-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="73679-117">stream オブジェクト用に新しいストレージオブジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="73679-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="73679-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="73679-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="73679-119">ストレージオブジェクトは、ストリームの現在の位置から開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="73679-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="73679-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="73679-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="73679-121">呼び出し元は、返されたストレージオブジェクトに対する読み取り/書き込みアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="73679-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="73679-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="73679-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="73679-123">ストレージオブジェクトは、位置0から開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="73679-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="73679-124">_lppstorageout_</span><span class="sxs-lookup"><span data-stu-id="73679-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="73679-125">読み上げストレージオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="73679-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="73679-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="73679-126">Return value</span></span>

<span data-ttu-id="73679-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="73679-127">S_OK</span></span> 
  
> <span data-ttu-id="73679-128">ストレージオブジェクトが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="73679-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73679-129">解説</span><span class="sxs-lookup"><span data-stu-id="73679-129">Remarks</span></span>

<span data-ttu-id="73679-130">**imapisupport:: istoragefromstream**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="73679-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="73679-131">サービスプロバイダーは、 **istoragefromstream**を呼び出して、特定のプロパティを開くために使用するストレージオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="73679-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="73679-132">[IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx)インターフェイスを独自に実装しているサービスプロバイダーは、 **istoragefromstream**を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="73679-132">Service providers that have their own implementation of the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="73679-133">**istoragefromstream**によって作成されたストレージオブジェクトは、ストリームの[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出して、参照カウントをインクリメントし、ストレージが解放されたときにカウントをデクリメントします。</span><span class="sxs-lookup"><span data-stu-id="73679-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="73679-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="73679-134">Notes to callers</span></span>

<span data-ttu-id="73679-135">いずれかのオブジェクトの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドが呼び出されたときに、 **IStorage**インターフェイスを持つプロパティを開くには、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="73679-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="73679-136">プロパティの読み取り/書き込み権限を持つ stream オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="73679-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="73679-137">プロパティストリームをストレージオブジェクトとして内部的にマークします。</span><span class="sxs-lookup"><span data-stu-id="73679-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="73679-138">ストレージオブジェクトを生成するには、 **istoragefromstream**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="73679-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="73679-139">このストレージオブジェクトへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="73679-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="73679-140">ストレージオブジェクトを使用する追加のインターフェイスを実装する場合は、ストレージオブジェクトをラップするオブジェクトを作成し、より高いレベルの[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="73679-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="73679-141">プロパティが**IStorage**を使用して作成された場合、 **IStream**インターフェイスで開くことを許可しません。</span><span class="sxs-lookup"><span data-stu-id="73679-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="73679-142">反対に、 **IStream**を使用して作成された場合、 **IStorage**インターフェイスでプロパティを開かないようにします。</span><span class="sxs-lookup"><span data-stu-id="73679-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="73679-143">1つの例外を除き、 **IStreamDocfile**インターフェイスを使用して、あるコンテナーから別のコンテナーに格納オブジェクトをストリームすることはできますが、 **openproperty**メソッドの lpinterface で IID_IStreamDocfile インターフェイス識別子を渡す必要があります。 __ パラメーター。</span><span class="sxs-lookup"><span data-stu-id="73679-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73679-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="73679-144">See also</span></span>



[<span data-ttu-id="73679-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="73679-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="73679-146">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="73679-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

