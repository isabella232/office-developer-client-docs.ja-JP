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
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325670"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="85536-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="85536-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="85536-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85536-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85536-105">メッセージストアの内部エントリ識別子を、メッセージングシステムによって使用可能なエントリ id に変換します。</span><span class="sxs-lookup"><span data-stu-id="85536-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85536-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="85536-106">Header file:</span></span>  <br/> |<span data-ttu-id="85536-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="85536-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="85536-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="85536-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="85536-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="85536-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="85536-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="85536-110">Called by:</span></span>  <br/> |<span data-ttu-id="85536-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="85536-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="85536-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="85536-112">Parameters</span></span>

 <span data-ttu-id="85536-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="85536-113">_ulFlags_</span></span>
  
> <span data-ttu-id="85536-114">順番フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="85536-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="85536-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="85536-115">The following flag can be set:</span></span>
    
<span data-ttu-id="85536-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="85536-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="85536-117">文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="85536-117">The strings are in Unicode format.</span></span> <span data-ttu-id="85536-118">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="85536-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="85536-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="85536-119">_szDLLName_</span></span>
  
> <span data-ttu-id="85536-120">順番メッセージストアプロバイダー DLL の名前。</span><span class="sxs-lookup"><span data-stu-id="85536-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="85536-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="85536-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="85536-122">順番メッセージストアの元のエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="85536-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="85536-123">_lporigentry_</span><span class="sxs-lookup"><span data-stu-id="85536-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="85536-124">順番元のエントリ識別子を含む[ENTRYID](entryid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="85536-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="85536-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="85536-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="85536-126">読み上げ新しいエントリ識別子のサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="85536-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="85536-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="85536-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="85536-128">読み上げ新しいエントリ識別子を含む**ENTRYID**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="85536-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85536-129">Return value</span><span class="sxs-lookup"><span data-stu-id="85536-129">Return value</span></span>

<span data-ttu-id="85536-130">なし。</span><span class="sxs-lookup"><span data-stu-id="85536-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85536-131">解説</span><span class="sxs-lookup"><span data-stu-id="85536-131">Remarks</span></span>

<span data-ttu-id="85536-132">メッセージストアオブジェクトは、そのメッセージストアとのサービスプロバイダ coresident にのみ意味がある内部エントリ識別子を保持します。</span><span class="sxs-lookup"><span data-stu-id="85536-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="85536-133">その他のメッセージングコンポーネントの場合、MAPI は、メッセージストアに属しているものとして認識できるようにするために、ラップされたバージョンの内部エントリ識別子を提供します。</span><span class="sxs-lookup"><span data-stu-id="85536-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="85536-134">coresident サービスプロバイダーには、必ず、元のラップされていないメッセージストアエントリ識別子を指定する必要があります。クライアントアプリケーションには常にラップされたバージョンが指定されている必要があります。これは、メッセージングドメインとその他のドメイン内の任意の場所で使用できます。</span><span class="sxs-lookup"><span data-stu-id="85536-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="85536-135">サービスプロバイダーは、 **WrapStoreEntryID**関数または[imapisupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md)メソッドのいずれかを使用して、メッセージストアエントリ識別子をラップできます。このメソッドは、 **WrapStoreEntryID**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="85536-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="85536-136">プロバイダーは、メッセージストアの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを公開するか、プロファイルセクションに書き込むとき、および**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) を公開するときに、エントリ識別子をラップする必要があります。プロパティ.</span><span class="sxs-lookup"><span data-stu-id="85536-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="85536-137">MAPI は、 [imapisession:: openmsgstore](imapisession-openmsgstore.md)呼び出しに応答するときに、メッセージストアエントリ識別子をラップします。</span><span class="sxs-lookup"><span data-stu-id="85536-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="85536-138">クライアントアプリケーションが、ラップされたメッセージストアエントリ識別子を mapi に渡すと ( [imapisession:: openentry](imapisession-openentry.md)呼び出しなど)、mapi は、 [IMSProvider:: Logon](imsprovider-logon.md) [などのプロバイダーメソッドを呼び出す前に、エントリ識別子をラップします。IMSProvider:: comparestoreids](imsprovider-comparestoreids.md)。</span><span class="sxs-lookup"><span data-stu-id="85536-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

