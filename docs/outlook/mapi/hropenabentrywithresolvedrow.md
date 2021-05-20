---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2eb643e0002e2159e3197d66e021aba0bb8c126f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429909"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="a1d49-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="a1d49-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="a1d49-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1d49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1d49-105">解決された行から **emsabpUID** を自動的に取得し **、entryID** を開く以外は [、HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)と同じ関数を実行します。</span><span class="sxs-lookup"><span data-stu-id="a1d49-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1d49-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a1d49-106">Header file:</span></span>  <br/> |<span data-ttu-id="a1d49-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="a1d49-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="a1d49-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="a1d49-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a1d49-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a1d49-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a1d49-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a1d49-110">Called by:</span></span>  <br/> |<span data-ttu-id="a1d49-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a1d49-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithResolvedRow(
  LPSRow prwResolved,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="a1d49-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a1d49-112">Parameters</span></span>

 <span data-ttu-id="a1d49-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="a1d49-113">_prwResolved_</span></span>
  
> <span data-ttu-id="a1d49-114">[in] **emsabpUID** を取得し **、entryID** を開くのに使用される解決済み行へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1d49-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="a1d49-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="a1d49-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="a1d49-116">[in]エントリ識別子を開くのに使用するアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="a1d49-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="a1d49-117">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a1d49-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="a1d49-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a1d49-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="a1d49-119">[in]  _lpEntryID_ パラメーターで指定されたエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="a1d49-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a1d49-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a1d49-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="a1d49-121">[in]開くアドレス帳エントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1d49-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="a1d49-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a1d49-122">_lpInterface_</span></span>
  
> <span data-ttu-id="a1d49-123">[in]開いているエントリへのアクセスに使用されるインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1d49-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="a1d49-124">NULL を渡す場合は、オブジェクトの標準インターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="a1d49-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="a1d49-125">メッセージング ユーザーの場合、標準インターフェイスは [IMailUser : IMAPIProp です](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="a1d49-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="a1d49-126">配布リストの場合 [、IDistList : IMAPIContainer](idistlistimapicontainer.md)であり、コンテナーの場合は [IABContainer : IMAPIContainer です](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="a1d49-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="a1d49-127">呼び出し元は  _、lpInterface を_ 適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。</span><span class="sxs-lookup"><span data-stu-id="a1d49-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="a1d49-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a1d49-128">_ulFlags_</span></span>
  
> <span data-ttu-id="a1d49-129">[in]エントリの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a1d49-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="a1d49-130">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a1d49-130">The following flags can be set:</span></span>
    
<span data-ttu-id="a1d49-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a1d49-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="a1d49-132">許可されるネットワークおよびクライアントの最大アクセス許可を使用してエントリを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="a1d49-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="a1d49-133">たとえば、クライアントに読み取りおよび書き込みアクセス許可がある場合、アドレス帳プロバイダーは読み取りおよび書き込みアクセス許可を持つエントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="a1d49-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="a1d49-134">クライアントは、開いているエントリの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出し、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得することで、付与されたアクセス レベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="a1d49-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="a1d49-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="a1d49-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="a1d49-136">名前解決を実行するには、オフライン アドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="a1d49-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="a1d49-137">たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a1d49-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="a1d49-138">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="a1d49-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="a1d49-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a1d49-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="a1d49-140">エントリが完全に開いて使用可能になる前に、呼び出しが成功する可能性があります。その後のエントリへの呼び出しがエラーを返す可能性を示します。</span><span class="sxs-lookup"><span data-stu-id="a1d49-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="a1d49-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="a1d49-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="a1d49-142">名前解決を実行する場合は、GAL のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="a1d49-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="a1d49-143">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="a1d49-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="a1d49-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a1d49-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="a1d49-145">読み取りおよび書き込みアクセス許可を持つエントリを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="a1d49-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="a1d49-146">既定では、読み取り専用アクセスでエントリが開くので、クライアントは、読み取りアクセス許可と書き込みアクセス許可が設定されているかどうかに関係なく、読み取りおよび書き込み権限が付与MAPI_MODIFY必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1d49-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="a1d49-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="a1d49-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="a1d49-148">名前解決を実行するためにオフライン アドレス帳を使用しない。</span><span class="sxs-lookup"><span data-stu-id="a1d49-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="a1d49-149">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="a1d49-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="a1d49-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="a1d49-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="a1d49-151">[out]開いたエントリの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1d49-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="a1d49-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="a1d49-152">_lppUnk_</span></span>
  
> <span data-ttu-id="a1d49-153">[out]開いたエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1d49-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

