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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409210"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="67826-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="67826-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="67826-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67826-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67826-105">メッセージ ストアの内部エントリ識別子を、メッセージング システムで使用できるエントリ識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="67826-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67826-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="67826-106">Header file:</span></span>  <br/> |<span data-ttu-id="67826-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67826-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="67826-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="67826-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="67826-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="67826-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="67826-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="67826-110">Called by:</span></span>  <br/> |<span data-ttu-id="67826-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="67826-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="67826-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="67826-112">Parameters</span></span>

 <span data-ttu-id="67826-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="67826-113">_ulFlags_</span></span>
  
> <span data-ttu-id="67826-114">[in]フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="67826-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="67826-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="67826-115">The following flag can be set:</span></span>
    
<span data-ttu-id="67826-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="67826-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="67826-117">文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="67826-117">The strings are in Unicode format.</span></span> <span data-ttu-id="67826-118">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="67826-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="67826-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="67826-119">_szDLLName_</span></span>
  
> <span data-ttu-id="67826-120">[in]メッセージ ストア プロバイダー DLL の名前。</span><span class="sxs-lookup"><span data-stu-id="67826-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="67826-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="67826-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="67826-122">[in]メッセージ ストアの元のエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="67826-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="67826-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="67826-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="67826-124">[in]元のエントリ [識別子を](entryid.md) 含む ENTRYID 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="67826-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="67826-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="67826-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="67826-126">[out]新しいエントリ識別子のサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="67826-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="67826-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="67826-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="67826-128">[out]新しいエントリ識別子を含 **む ENTRYID** 構造体へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="67826-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="67826-129">Return value</span><span class="sxs-lookup"><span data-stu-id="67826-129">Return value</span></span>

<span data-ttu-id="67826-130">なし。</span><span class="sxs-lookup"><span data-stu-id="67826-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67826-131">注釈</span><span class="sxs-lookup"><span data-stu-id="67826-131">Remarks</span></span>

<span data-ttu-id="67826-132">メッセージ ストア オブジェクトは内部エントリ識別子を保持します。これは、そのメッセージ ストアを持つサービス プロバイダーの coresident にとってのみ意味があります。</span><span class="sxs-lookup"><span data-stu-id="67826-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="67826-133">その他のメッセージング コンポーネントの場合、MAPI は、メッセージ ストアに属すると認識できる、ラップされたバージョンの内部エントリ識別子を提供します。</span><span class="sxs-lookup"><span data-stu-id="67826-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="67826-134">Coresident サービス プロバイダーには、常に元のラップされていないメッセージ ストア エントリ識別子を指定する必要があります。クライアント アプリケーションには、常にラップされたバージョンを指定する必要があります。その後、メッセージング ドメイン内および他のドメインの任意の場所で使用できます。</span><span class="sxs-lookup"><span data-stu-id="67826-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="67826-135">サービス プロバイダーは **、WrapStoreEntryID 関数または WRAPStoreEntryID** 関数を呼び出す [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)メソッドを使用して、メッセージ ストアエントリ識別子をラップできます。 </span><span class="sxs-lookup"><span data-stu-id="67826-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="67826-136">プロバイダーは、メッセージ ストア **の PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを公開する場合、またはプロファイル セクションに書き込む場合、および **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) プロパティを公開するときに、エントリ識別子をラップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="67826-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="67826-137">MAPI は [、IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) 呼び出しに応答するときにメッセージ ストアエントリ識別子をラップします。</span><span class="sxs-lookup"><span data-stu-id="67826-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="67826-138">クライアント アプリケーションが [、IMAPISession::OpenEntry](imapisession-openentry.md) 呼び出しなど、ラップされたメッセージ ストアエントリ識別子を MAPI に渡す場合、MAPI はエントリ識別子をアンラップしてから、そのエントリ識別子を使用して [IMSProvider::Logon](imsprovider-logon.md) や [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md)などのプロバイダー メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="67826-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

