---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2eb643e0002e2159e3197d66e021aba0bb8c126f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347776"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="82233-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="82233-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="82233-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82233-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82233-105">[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)と同じ機能を実行します。ただし、 **emsabpUID**を解決済みの行から自動的に取得し、 **entryID**を開きます。</span><span class="sxs-lookup"><span data-stu-id="82233-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82233-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="82233-106">Header file:</span></span>  <br/> |<span data-ttu-id="82233-107">abhelp .h</span><span class="sxs-lookup"><span data-stu-id="82233-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="82233-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="82233-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="82233-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="82233-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="82233-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="82233-110">Called by:</span></span>  <br/> |<span data-ttu-id="82233-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="82233-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="82233-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="82233-112">Parameters</span></span>

 <span data-ttu-id="82233-113">_prwresolved 済み_</span><span class="sxs-lookup"><span data-stu-id="82233-113">_prwResolved_</span></span>
  
> <span data-ttu-id="82233-114">順番**emsabpUID**を取得し、 **entryID**を開くために使用される解決済みの行へのポインター。</span><span class="sxs-lookup"><span data-stu-id="82233-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="82233-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="82233-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="82233-116">順番エントリ識別子を開くために使用されるアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="82233-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="82233-117">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="82233-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="82233-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="82233-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="82233-119">順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。</span><span class="sxs-lookup"><span data-stu-id="82233-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="82233-120">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="82233-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="82233-121">順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="82233-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="82233-122">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="82233-122">_lpInterface_</span></span>
  
> <span data-ttu-id="82233-123">順番開いているエントリへのアクセスに使用されるインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="82233-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="82233-124">NULL を渡すと、オブジェクトの標準インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="82233-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="82233-125">メッセージングユーザーの場合、標準インターフェイスは[imailuser: imapiprop](imailuserimapiprop.md)です。</span><span class="sxs-lookup"><span data-stu-id="82233-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="82233-126">配布リストの場合、 [idistlist: IMAPIContainer](idistlistimapicontainer.md)およびコンテナーの場合は、 [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)になります。</span><span class="sxs-lookup"><span data-stu-id="82233-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="82233-127">呼び出し元は、 _lpinterface_を適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。</span><span class="sxs-lookup"><span data-stu-id="82233-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="82233-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="82233-128">_ulFlags_</span></span>
  
> <span data-ttu-id="82233-129">順番エントリが開かれる方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="82233-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="82233-130">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="82233-130">The following flags can be set:</span></span>
    
<span data-ttu-id="82233-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="82233-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="82233-132">許可された最大ネットワークおよびクライアントアクセス許可でエントリが開かれることを要求します。</span><span class="sxs-lookup"><span data-stu-id="82233-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="82233-133">たとえば、クライアントが読み取りおよび書き込みアクセス許可を持っている場合、アドレス帳プロバイダーは、読み取りおよび書き込みアクセス許可を持つエントリを開こうとします。</span><span class="sxs-lookup"><span data-stu-id="82233-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="82233-134">クライアントは、開いているエントリの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得することによって付与されたアクセスレベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="82233-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="82233-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="82233-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="82233-136">名前解決を実行するのにオフラインアドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="82233-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="82233-137">たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="82233-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="82233-138">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="82233-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="82233-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="82233-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="82233-140">呼び出しが正常に完了します。エントリが完全に開かれて使用可能になる前に、エントリへの以降の呼び出しでエラーが返される可能性があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="82233-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="82233-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="82233-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="82233-142">名前解決を実行するには、GAL のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="82233-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="82233-143">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="82233-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="82233-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="82233-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="82233-145">読み取りと書き込みのアクセス許可を使用して、エントリを開くように要求します。</span><span class="sxs-lookup"><span data-stu-id="82233-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="82233-146">既定では、エントリは読み取り専用アクセスで開かれるため、クライアントは、MAPI_MODIFY が設定されているかどうかに関係なく、読み取りおよび書き込みアクセス許可が付与されたことを想定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="82233-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="82233-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="82233-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="82233-148">では、オフラインアドレス帳を使用して名前解決を実行しません。</span><span class="sxs-lookup"><span data-stu-id="82233-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="82233-149">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="82233-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="82233-150">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="82233-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="82233-151">読み上げ開かれた項目の種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="82233-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="82233-152">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="82233-152">_lppUnk_</span></span>
  
> <span data-ttu-id="82233-153">読み上げ開かれたエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="82233-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

