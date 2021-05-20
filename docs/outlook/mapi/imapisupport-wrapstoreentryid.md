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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430449"
---
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="d9ca1-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="d9ca1-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="d9ca1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9ca1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9ca1-105">メッセージ ストアの内部エントリ識別子を MAPI 標準形式のエントリ識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="d9ca1-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="d9ca1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9ca1-106">Parameters</span></span>

 <span data-ttu-id="d9ca1-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="d9ca1-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="d9ca1-108">[in]  _lpOrigEntry_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="d9ca1-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="d9ca1-109">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="d9ca1-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="d9ca1-110">[in]メッセージ ストアのプライベート エントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9ca1-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="d9ca1-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="d9ca1-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="d9ca1-112">[out]  _lppWrappedEntry_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9ca1-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="d9ca1-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="d9ca1-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="d9ca1-114">[out]ラップされたエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9ca1-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9ca1-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9ca1-115">Return value</span></span>

<span data-ttu-id="d9ca1-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9ca1-116">S_OK</span></span> 
  
> <span data-ttu-id="d9ca1-117">エントリ識別子が正常にラップされました。</span><span class="sxs-lookup"><span data-stu-id="d9ca1-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9ca1-118">注釈</span><span class="sxs-lookup"><span data-stu-id="d9ca1-118">Remarks</span></span>

<span data-ttu-id="d9ca1-119">**IMAPISupport::WrapStoreEntryID** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="d9ca1-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="d9ca1-120">サービス プロバイダーは **WrapStoreEntryID** を使用して、MAPI がストアの内部エントリ識別子をラップするメッセージ ストアのエントリ識別子を生成します。</span><span class="sxs-lookup"><span data-stu-id="d9ca1-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d9ca1-121">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d9ca1-121">Notes to callers</span></span>

<span data-ttu-id="d9ca1-122">クライアントがメッセージ ストアの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して **PR_STORE_ENTRYID** ([PidTagStoreEntryId)](pidtagstoreentryid-canonical-property.md)プロパティを取得し、メッセージ ストアでプライベート形式のエントリ識別子を使用する場合は **、WrapStoreEntryID** を呼び出し  _、lppWrappedEntry_ パラメーターが指すエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="d9ca1-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="d9ca1-123">[IMSProvider::Logon](imsprovider-logon.md)メソッドと[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)メソッドの呼び出しは、常にストアのプライベート エントリ識別子を取得します。ラップされたバージョンは、クライアント アプリケーションと MAPI の間でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="d9ca1-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="d9ca1-124">エントリ識別子の使用が完了したら [、MAPIFreeBuffer](mapifreebuffer.md)関数を使用して _、lppWrappedEntry_ パラメーターが指すエントリ識別子のメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="d9ca1-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d9ca1-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9ca1-125">See also</span></span>



[<span data-ttu-id="d9ca1-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="d9ca1-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="d9ca1-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="d9ca1-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="d9ca1-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="d9ca1-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="d9ca1-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="d9ca1-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="d9ca1-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d9ca1-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d9ca1-131">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9ca1-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

