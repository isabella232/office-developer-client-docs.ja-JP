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
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347790"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="94a28-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="94a28-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="94a28-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94a28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94a28-105">**pEmsmdbUID**によって識別される Exchange アドレス帳を使用して、 **entryID**を開きます。</span><span class="sxs-lookup"><span data-stu-id="94a28-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="94a28-106">この関数は、 [IAddrBook::D etails](iaddrbook-details.md)と同じように動作します。ただし、この関数を使用すると、予期される Exchange アドレス帳プロバイダーを使用して[IAddrBook:: openentry](iaddrbook-openentry.md)が開かれることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="94a28-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94a28-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="94a28-107">Header file:</span></span>  <br/> |<span data-ttu-id="94a28-108">abhelp .h</span><span class="sxs-lookup"><span data-stu-id="94a28-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="94a28-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="94a28-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="94a28-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="94a28-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="94a28-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="94a28-111">Called by:</span></span>  <br/> |<span data-ttu-id="94a28-112">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="94a28-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="94a28-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="94a28-113">Parameters</span></span>

 <span data-ttu-id="94a28-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="94a28-114">_pmsess_</span></span>
  
> <span data-ttu-id="94a28-115">順番ログオンしている**imapisession**。</span><span class="sxs-lookup"><span data-stu-id="94a28-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="94a28-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="94a28-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="94a28-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="94a28-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="94a28-118">順番この関数がエントリ識別子の詳細を表示するために使用する exchange アドレス帳プロバイダーを含む exchange サービスを識別する**emsmdbUID**へのポインター。</span><span class="sxs-lookup"><span data-stu-id="94a28-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="94a28-119">受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出しは[IAddrBook::D etails](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="94a28-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="94a28-120">このパラメーターが NULL またはゼロ MAPIUID の場合、この関数は[IAddrBook::D etails](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="94a28-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="94a28-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="94a28-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="94a28-122">順番エントリ識別子を開くために使用されるアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="94a28-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="94a28-123">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="94a28-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="94a28-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="94a28-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="94a28-125">順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。</span><span class="sxs-lookup"><span data-stu-id="94a28-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="94a28-126">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="94a28-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="94a28-127">順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="94a28-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="94a28-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="94a28-128">_ulFlags_</span></span>
  
> <span data-ttu-id="94a28-129">順番エントリが開かれる方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="94a28-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="94a28-130">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="94a28-130">The following flags can be set:</span></span>
    
<span data-ttu-id="94a28-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="94a28-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="94a28-132">許可された最大ネットワークおよびクライアントアクセス許可でエントリが開かれることを要求します。</span><span class="sxs-lookup"><span data-stu-id="94a28-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="94a28-133">たとえば、クライアントが読み取りおよび書き込みアクセス許可を持っている場合、アドレス帳プロバイダーは、読み取りおよび書き込みアクセス許可を持つエントリを開こうとします。</span><span class="sxs-lookup"><span data-stu-id="94a28-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="94a28-134">クライアントは、開いているエントリの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得することによって付与されたアクセスレベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="94a28-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="94a28-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="94a28-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="94a28-136">名前解決を実行するのにオフラインアドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="94a28-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="94a28-137">たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="94a28-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="94a28-138">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="94a28-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="94a28-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="94a28-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="94a28-140">呼び出しが正常に完了します。エントリが完全に開かれて使用可能になる前に、エントリへの以降の呼び出しでエラーが返される可能性があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="94a28-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="94a28-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="94a28-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="94a28-142">名前解決を実行するには、GAL のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="94a28-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="94a28-143">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="94a28-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="94a28-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="94a28-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="94a28-145">読み取りと書き込みのアクセス許可を使用して、エントリを開くように要求します。</span><span class="sxs-lookup"><span data-stu-id="94a28-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="94a28-146">既定では、エントリは読み取り専用アクセスで開かれるため、クライアントは、MAPI_MODIFY が設定されているかどうかに関係なく、読み取りおよび書き込みアクセス許可が付与されたことを想定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="94a28-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="94a28-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="94a28-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="94a28-148">では、オフラインアドレス帳を使用して名前解決を実行しません。</span><span class="sxs-lookup"><span data-stu-id="94a28-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="94a28-149">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="94a28-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

