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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 25c04f8dee012f4985db98df7d1b3ae5536ef6b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800802"
---
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="6df13-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="6df13-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="6df13-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6df13-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6df13-105">MAPI の標準的な形式のエントリ id をメッセージ ・ ストアの内部のエントリの識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="6df13-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="6df13-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6df13-106">Parameters</span></span>

 <span data-ttu-id="6df13-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="6df13-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="6df13-108">[in]_LpOrigEntry_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="6df13-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="6df13-109">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="6df13-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="6df13-110">[in]メッセージ ・ ストアのプライベート エントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6df13-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="6df13-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="6df13-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="6df13-112">[out]_LppWrappedEntry_パラメーターで指定されたエントリの識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6df13-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="6df13-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="6df13-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="6df13-114">[out]ラップされたエントリの識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6df13-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6df13-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6df13-115">Return value</span></span>

<span data-ttu-id="6df13-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6df13-116">S_OK</span></span> 
  
> <span data-ttu-id="6df13-117">エントリ id が正常に折り返されます。</span><span class="sxs-lookup"><span data-stu-id="6df13-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6df13-118">備考</span><span class="sxs-lookup"><span data-stu-id="6df13-118">Remarks</span></span>

<span data-ttu-id="6df13-119">サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::WrapStoreEntryID**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="6df13-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="6df13-120">サービス プロバイダーは、ストアの内部のエントリの識別子をラップするメッセージ ・ ストアのエントリ識別子を生成する MAPI を使用して**WrapStoreEntryID**を使用します。</span><span class="sxs-lookup"><span data-stu-id="6df13-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6df13-121">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="6df13-121">Notes to callers</span></span>

<span data-ttu-id="6df13-122">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) のプロパティと、メッセージ ストアを取得するためにプライベートの形式で、エントリ id を使用して、クライアントが、メッセージ ・ ストアの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すときは、 **WrapStoreEntryID を呼び出す**し、 _lppWrappedEntry_パラメーターで指定されたエントリの識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="6df13-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="6df13-123">[IMSProvider::Logon](imsprovider-logon.md)と[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)メソッドの呼び出しは常にストアのプライベート エントリの識別子を取得します。ラップのバージョンは、クライアント アプリケーションと MAPI の間でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="6df13-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="6df13-124">エントリの識別子を使用してが完了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用して、 _lppWrappedEntry_パラメーターで示されるエントリ id 用のメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="6df13-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6df13-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="6df13-125">See also</span></span>



[<span data-ttu-id="6df13-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="6df13-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="6df13-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="6df13-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="6df13-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="6df13-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="6df13-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="6df13-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="6df13-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6df13-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6df13-131">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6df13-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

