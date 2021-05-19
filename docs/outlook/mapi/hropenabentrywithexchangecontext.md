---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434054"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="5e826-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="5e826-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="5e826-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e826-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e826-105">**pEmsmdbUID** で識別Exchangeアドレス帳を使用して entryID を開きます。 </span><span class="sxs-lookup"><span data-stu-id="5e826-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="5e826-106">この関数は[、IAddrBook::D etails](iaddrbook-details.md)と同様に動作しますが、この関数を使用すると[、IAddrBook::OpenEntry](iaddrbook-openentry.md)が予期される Exchange アドレス帳プロバイダーを使用して開きます。</span><span class="sxs-lookup"><span data-stu-id="5e826-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5e826-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5e826-107">Header file:</span></span>  <br/> |<span data-ttu-id="5e826-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="5e826-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="5e826-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="5e826-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="5e826-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="5e826-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="5e826-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5e826-111">Called by:</span></span>  <br/> |<span data-ttu-id="5e826-112">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="5e826-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="5e826-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e826-113">Parameters</span></span>

 <span data-ttu-id="5e826-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="5e826-114">_pmsess_</span></span>
  
> <span data-ttu-id="5e826-115">[in]ログオンしている **IMAPISession**。</span><span class="sxs-lookup"><span data-stu-id="5e826-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="5e826-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="5e826-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="5e826-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="5e826-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="5e826-118">[in]この関数がエントリ識別子の詳細を表示するために使用する Exchange アドレス帳プロバイダーを含む Exchange サービスを識別する **emsmdbUID** へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5e826-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="5e826-119">受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出し[は IAddrBook::D etails](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="5e826-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="5e826-120">このパラメーターが NULL または 0 の MAPIUID の場合、この関数は [IAddrBook::D同様に動作します](iaddrbook-details.md)。</span><span class="sxs-lookup"><span data-stu-id="5e826-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="5e826-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="5e826-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="5e826-122">[in]エントリ識別子を開くのに使用するアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="5e826-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="5e826-123">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="5e826-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="5e826-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5e826-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="5e826-125">[in]  _lpEntryID_ パラメーターで指定されたエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="5e826-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5e826-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5e826-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="5e826-127">[in]開くアドレス帳エントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5e826-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="5e826-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e826-128">_ulFlags_</span></span>
  
> <span data-ttu-id="5e826-129">[in]エントリの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5e826-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="5e826-130">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5e826-130">The following flags can be set:</span></span>
    
<span data-ttu-id="5e826-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5e826-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="5e826-132">許可されるネットワークおよびクライアントの最大アクセス許可を使用してエントリを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="5e826-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="5e826-133">たとえば、クライアントに読み取りおよび書き込みアクセス許可がある場合、アドレス帳プロバイダーは読み取りおよび書き込みアクセス許可を持つエントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="5e826-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="5e826-134">クライアントは、開いているエントリの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出し、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得することで、付与されたアクセス レベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5e826-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="5e826-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="5e826-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="5e826-136">名前解決を実行するには、オフライン アドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="5e826-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="5e826-137">たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5e826-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="5e826-138">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5e826-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="5e826-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5e826-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="5e826-140">エントリが完全に開いて使用可能になる前に、呼び出しが成功する可能性があります。その後のエントリへの呼び出しがエラーを返す可能性を示します。</span><span class="sxs-lookup"><span data-stu-id="5e826-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="5e826-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="5e826-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="5e826-142">名前解決を実行する場合は、GAL のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="5e826-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="5e826-143">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5e826-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="5e826-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5e826-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="5e826-145">読み取りおよび書き込みアクセス許可を持つエントリを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="5e826-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="5e826-146">既定では、読み取り専用アクセスでエントリが開くので、クライアントは、読み取りアクセス許可と書き込みアクセス許可が設定されているかどうかに関係なく、読み取りおよび書き込み権限が付与MAPI_MODIFY必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e826-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="5e826-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="5e826-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="5e826-148">名前解決を実行するためにオフライン アドレス帳を使用しない。</span><span class="sxs-lookup"><span data-stu-id="5e826-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="5e826-149">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5e826-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

