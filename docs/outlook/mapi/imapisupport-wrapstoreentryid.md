---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a623ef24f76dae93bfc13e6613e885a120f3278e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341287"
---
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="534eb-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="534eb-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="534eb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="534eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="534eb-105">メッセージストアの内部エントリ識別子を MAPI 標準形式のエントリ id に変換します。</span><span class="sxs-lookup"><span data-stu-id="534eb-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="534eb-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="534eb-106">Parameters</span></span>

 <span data-ttu-id="534eb-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="534eb-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="534eb-108">順番_lporigentry_パラメーターによって指摘されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="534eb-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="534eb-109">_lporigentry_</span><span class="sxs-lookup"><span data-stu-id="534eb-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="534eb-110">順番メッセージストアのプライベートエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="534eb-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="534eb-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="534eb-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="534eb-112">読み上げ_lppWrappedEntry_パラメーターによって示されるエントリ識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="534eb-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="534eb-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="534eb-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="534eb-114">読み上げラップされたエントリ識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="534eb-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="534eb-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="534eb-115">Return value</span></span>

<span data-ttu-id="534eb-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="534eb-116">S_OK</span></span> 
  
> <span data-ttu-id="534eb-117">エントリ識別子が正常にラップされました。</span><span class="sxs-lookup"><span data-stu-id="534eb-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="534eb-118">解説</span><span class="sxs-lookup"><span data-stu-id="534eb-118">Remarks</span></span>

<span data-ttu-id="534eb-119">**imapisupport:: WrapStoreEntryID**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="534eb-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="534eb-120">サービスプロバイダーは**WrapStoreEntryID**を使用して、ストアの内部エントリ識別子をラップするメッセージストアのエントリ識別子を MAPI で生成します。</span><span class="sxs-lookup"><span data-stu-id="534eb-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="534eb-121">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="534eb-121">Notes to callers</span></span>

<span data-ttu-id="534eb-122">クライアントがメッセージストアの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) プロパティを取得し、メッセージストアがプライベート形式のエントリ識別子を使用する場合は、WrapStoreEntryID を呼び出します。 \*\*\*\* を指定し、 _lppWrappedEntry_パラメーターで指定されたエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="534eb-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="534eb-123">[IMSProvider:: Logon](imsprovider-logon.md)および[IMSLogon:: compareentryids](imslogon-compareentryids.md)メソッドの呼び出しは、常にストアの秘密エントリ識別子を取得します。ラップされたバージョンは、クライアントアプリケーションと MAPI 間でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="534eb-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="534eb-124">エントリ識別子の使用が終了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用して、 _lppWrappedEntry_パラメーターで指定されたエントリ識別子のメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="534eb-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="534eb-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="534eb-125">See also</span></span>



[<span data-ttu-id="534eb-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="534eb-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="534eb-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="534eb-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="534eb-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="534eb-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="534eb-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="534eb-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="534eb-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="534eb-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="534eb-131">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="534eb-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

