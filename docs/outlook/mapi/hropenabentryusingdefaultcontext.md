---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f60c4d3761694439d10b073fda5bc36443c13e43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347825"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="a02e6-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="a02e6-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="a02e6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a02e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a02e6-105">[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)と同じ機能を実行します。ただし、 _pEmsmdbUID_パラメーターとして従来の**emsmdbUID**を使用する点が異なります。</span><span class="sxs-lookup"><span data-stu-id="a02e6-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="a02e6-106">[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)の呼び出しに対して正しい**emsmdbUID**を取得できない場合は、この関数を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="a02e6-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a02e6-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a02e6-107">Header file:</span></span>  <br/> |<span data-ttu-id="a02e6-108">abhelp .h</span><span class="sxs-lookup"><span data-stu-id="a02e6-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="a02e6-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="a02e6-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="a02e6-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="a02e6-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="a02e6-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a02e6-111">Called by:</span></span>  <br/> |<span data-ttu-id="a02e6-112">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="a02e6-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryUsingDefaultContext(
  LPMAPISESSION pmsess,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="a02e6-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a02e6-113">Parameters</span></span>

 <span data-ttu-id="a02e6-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="a02e6-114">_pmsess_</span></span>
  
> <span data-ttu-id="a02e6-115">順番ログオンしている**imapisession**。</span><span class="sxs-lookup"><span data-stu-id="a02e6-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="a02e6-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a02e6-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="a02e6-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="a02e6-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="a02e6-118">順番エントリ識別子を開くために使用されるアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="a02e6-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="a02e6-119">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a02e6-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="a02e6-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a02e6-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="a02e6-121">順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。</span><span class="sxs-lookup"><span data-stu-id="a02e6-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a02e6-122">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="a02e6-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="a02e6-123">順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a02e6-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="a02e6-124">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="a02e6-124">_lpInterface_</span></span>
  
> <span data-ttu-id="a02e6-125">順番開いているエントリへのアクセスに使用されるインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a02e6-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="a02e6-126">NULL を渡すと、オブジェクトの標準インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="a02e6-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="a02e6-127">メッセージングユーザーの場合、標準インターフェイスは[imailuser: imapiprop](imailuserimapiprop.md)です。</span><span class="sxs-lookup"><span data-stu-id="a02e6-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="a02e6-128">配布リストの場合、これは[idistlist: IMAPIContainer](idistlistimapicontainer.md)で、コンテナーの場合は[IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)です。</span><span class="sxs-lookup"><span data-stu-id="a02e6-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="a02e6-129">呼び出し元は、 _lpinterface_を適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。</span><span class="sxs-lookup"><span data-stu-id="a02e6-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="a02e6-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a02e6-130">_ulFlags_</span></span>
  
> <span data-ttu-id="a02e6-131">順番エントリが開かれる方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a02e6-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="a02e6-132">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a02e6-132">The following flags can be set:</span></span>
    
<span data-ttu-id="a02e6-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a02e6-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="a02e6-134">許可された最大ネットワークおよびクライアントアクセス許可でエントリが開かれることを要求します。</span><span class="sxs-lookup"><span data-stu-id="a02e6-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="a02e6-135">たとえば、クライアントが読み取りおよび書き込みアクセス許可を持っている場合、アドレス帳プロバイダーは、読み取りおよび書き込みアクセス許可を持つエントリを開こうとします。</span><span class="sxs-lookup"><span data-stu-id="a02e6-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="a02e6-136">クライアントは、開いているエントリの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得することによって付与されたアクセスレベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="a02e6-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="a02e6-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="a02e6-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="a02e6-138">名前解決を実行するのにオフラインアドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="a02e6-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="a02e6-139">たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a02e6-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="a02e6-140">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a02e6-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="a02e6-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a02e6-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="a02e6-142">呼び出しが正常に完了します。エントリが完全に開かれて使用可能になる前に、エントリへの以降の呼び出しでエラーが返される可能性があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="a02e6-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="a02e6-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="a02e6-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="a02e6-144">名前解決を実行するには、GAL のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="a02e6-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="a02e6-145">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a02e6-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="a02e6-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a02e6-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="a02e6-147">読み取りと書き込みのアクセス許可を使用して、エントリを開くように要求します。</span><span class="sxs-lookup"><span data-stu-id="a02e6-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="a02e6-148">既定では、エントリは読み取り専用アクセスで開かれるため、クライアントは、MAPI_MODIFY が設定されているかどうかに関係なく、読み取りおよび書き込みアクセス許可が付与されたことを想定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a02e6-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="a02e6-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="a02e6-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="a02e6-150">では、オフラインアドレス帳を使用して名前解決を実行しません。</span><span class="sxs-lookup"><span data-stu-id="a02e6-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="a02e6-151">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a02e6-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="a02e6-152">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="a02e6-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="a02e6-153">読み上げ開かれた項目の種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a02e6-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="a02e6-154">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="a02e6-154">_lppUnk_</span></span>
  
> <span data-ttu-id="a02e6-155">読み上げ開かれたエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a02e6-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

