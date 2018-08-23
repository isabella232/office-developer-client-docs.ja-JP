---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fcedaf689db8280b4649662ba61c8468d0f98305
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800306"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="041af-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="041af-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="041af-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="041af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="041af-105">**PEmsmdbUID**によって識別される、Exchange アドレス帳を使用して**エントリ Id**が表示されます。</span><span class="sxs-lookup"><span data-stu-id="041af-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="041af-106">この関数は、予想される Exchange アドレス帳プロバイダーを使用して、[アドレス帳コンテナー](iaddrbook-openentry.md)を開くことにより、この関数を使用することを除いて[IAddrBook::Details](iaddrbook-details.md)に同様に動作します。</span><span class="sxs-lookup"><span data-stu-id="041af-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="041af-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="041af-107">Header file:</span></span>  <br/> |<span data-ttu-id="041af-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="041af-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="041af-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="041af-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="041af-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="041af-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="041af-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="041af-111">Called by:</span></span>  <br/> |<span data-ttu-id="041af-112">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="041af-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="041af-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="041af-113">Parameters</span></span>

 <span data-ttu-id="041af-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="041af-114">_pmsess_</span></span>
  
> <span data-ttu-id="041af-115">[in]**IMAPISession**にログオンします。</span><span class="sxs-lookup"><span data-stu-id="041af-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="041af-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="041af-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="041af-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="041af-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="041af-118">[in]エントリ id の詳細を表示するのにはこの関数を使用する必要があります Exchange のアドレス帳プロバイダーが含まれている Exchange サービスを識別する**emsmdbUID**へのポインター。</span><span class="sxs-lookup"><span data-stu-id="041af-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="041af-119">受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子でない場合は、このパラメーターは無視され、関数呼び出しは、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="041af-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="041af-120">このパラメーターが NULL またはゼロの MAPIUID の場合は、この関数は、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="041af-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="041af-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="041af-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="041af-122">[in]アドレス帳のエントリ id を開くために使用します。</span><span class="sxs-lookup"><span data-stu-id="041af-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="041af-123">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="041af-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="041af-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="041af-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="041af-125">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="041af-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="041af-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="041af-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="041af-127">[in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="041af-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="041af-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="041af-128">_ulFlags_</span></span>
  
> <span data-ttu-id="041af-129">[in]エントリを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="041af-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="041af-130">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="041af-130">The following flags can be set:</span></span>
    
<span data-ttu-id="041af-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="041af-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="041af-132">最大許可されたネットワークとクライアントのアクセス許可を持つエントリを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="041af-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="041af-133">などの場合、クライアントでは、読み取りし、書き込みのアクセス許可、アドレス帳プロバイダーしようと読み取りでエントリを開き、書き込みのアクセス許可。</span><span class="sxs-lookup"><span data-stu-id="041af-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="041af-134">クライアントは、[open] エントリの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すと、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得するが許可されているアクセス レベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="041af-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="041af-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="041af-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="041af-136">オフライン アドレス帳のみを使用すると、名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="041af-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="041af-137">たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。</span><span class="sxs-lookup"><span data-stu-id="041af-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="041af-138">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="041af-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="041af-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="041af-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="041af-140">成功する可能性のあるエントリは、完全にオープンになり、エントリへの以降の呼び出しがエラーを返す可能性があることを示す前に呼び出しを使用できます。</span><span class="sxs-lookup"><span data-stu-id="041af-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="041af-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="041af-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="041af-142">GAL のみを使用すると、名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="041af-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="041af-143">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="041af-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="041af-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="041af-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="041af-145">エントリで開くことの要求は、アクセス許可を読み書きします。</span><span class="sxs-lookup"><span data-stu-id="041af-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="041af-146">エントリは読み取り専用アクセスで開くとき、既定であるために読み書き権限が与えられている MAPI_MODIFY が設定されているかどうかに関係なくクライアントを想定しません。</span><span class="sxs-lookup"><span data-stu-id="041af-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="041af-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="041af-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="041af-148">名前解決を実行するのには、オフライン アドレス帳を使用しません。</span><span class="sxs-lookup"><span data-stu-id="041af-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="041af-149">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="041af-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

