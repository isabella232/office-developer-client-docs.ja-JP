---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aff46cca7a7d530b2eede1790176058e3b91abc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804229"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="a2718-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="a2718-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="a2718-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a2718-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a2718-105">メッセージング システムがメッセージ ストアの内部のエントリの識別子をより使用可能なエントリ id に変換します。</span><span class="sxs-lookup"><span data-stu-id="a2718-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2718-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a2718-106">Header file:</span></span>  <br/> |<span data-ttu-id="a2718-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a2718-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a2718-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a2718-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a2718-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a2718-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a2718-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a2718-110">Called by:</span></span>  <br/> |<span data-ttu-id="a2718-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a2718-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
WrapStoreEntryID(
  ULONG ulFlags,
  LPSTR szDLLName,
  ULONG cbOrigEntry,
  LPENTRYID lpOrigEntry,
  ULONG * lpcbWrappedEntry,
  LPENTRYID * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="a2718-112">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="a2718-112">Parameters</span></span>

 <span data-ttu-id="a2718-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a2718-113">_ulFlags_</span></span>
  
> <span data-ttu-id="a2718-114">[in]フラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a2718-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="a2718-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a2718-115">The following flag can be set:</span></span>
    
<span data-ttu-id="a2718-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a2718-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a2718-117">文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="a2718-117">The strings are in Unicode format.</span></span> <span data-ttu-id="a2718-118">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="a2718-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="a2718-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="a2718-119">_szDLLName_</span></span>
  
> <span data-ttu-id="a2718-120">[in]メッセージ ストア プロバイダーの DLL の名前。</span><span class="sxs-lookup"><span data-stu-id="a2718-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="a2718-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="a2718-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="a2718-122">[in]メッセージ ・ ストアの元のエントリ id のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="a2718-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="a2718-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="a2718-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="a2718-124">[in]元のエントリ id が含まれている[エントリ ID](entryid.md)の構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a2718-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="a2718-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="a2718-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="a2718-126">[out]バイト単位で、新しいエントリ id のサイズへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a2718-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="a2718-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="a2718-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="a2718-128">[out]新しいエントリの識別子を含む**エントリ ID**の構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a2718-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a2718-129">Return value</span><span class="sxs-lookup"><span data-stu-id="a2718-129">Return value</span></span>

<span data-ttu-id="a2718-130">なし。</span><span class="sxs-lookup"><span data-stu-id="a2718-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2718-131">注釈</span><span class="sxs-lookup"><span data-stu-id="a2718-131">Remarks</span></span>

<span data-ttu-id="a2718-132">メッセージ ストアのオブジェクトは、そのメッセージ ・ ストアのサービス プロバイダーの coresident にのみ意味を持つエントリの内部識別子を保持します。</span><span class="sxs-lookup"><span data-stu-id="a2718-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="a2718-133">その他のメッセージング コンポーネントでは、MAPI には、ラップされたメッセージ ・ ストアに属していると認識可能な内部のエントリ id のバージョンが用意されています。</span><span class="sxs-lookup"><span data-stu-id="a2718-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="a2718-134">Coresident サービス ・ プロバイダーは常に指定する元のラップが解除されたメッセージ ストアのエントリ id です。クライアント アプリケーションは、常にでは、その使用可能な任意の場所のメッセージング ドメインと他のドメインに、ラップされたバージョンを指定してする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2718-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="a2718-135">サービス プロバイダーは、 **WrapStoreEntryID**関数または**WrapStoreEntryID**関数を呼び出し、 [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)メソッドのいずれかを使用して、メッセージ ストアのエントリの識別子を折り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="a2718-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="a2718-136">プロバイダーはメッセージ ストアの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) を公開するときのエントリ id をラップする必要がありますプロパティまたは書き込みを行うことと、[プロファイル] セクションに**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) を公開するときにプロパティです。</span><span class="sxs-lookup"><span data-stu-id="a2718-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="a2718-137">[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)の呼び出しに応答する場合、MAPI は、メッセージ ストアのエントリの識別子をラップします。</span><span class="sxs-lookup"><span data-stu-id="a2718-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="a2718-138">クライアント アプリケーションでは、MAPI にラップされたメッセージ ストアのエントリの識別子を渡しますと、の呼び出しでは、 [IMAPISession::OpenEntry](imapisession-openentry.md) MAPI のラップを解除のエントリ id [IMSProvider::Logon](imsprovider-logon.md)や[などのプロバイダーのメソッドを呼び出すために使用する前にIMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md)。</span><span class="sxs-lookup"><span data-stu-id="a2718-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

