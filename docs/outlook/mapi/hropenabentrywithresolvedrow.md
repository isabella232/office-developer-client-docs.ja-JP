---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0e39f4edc871b49675f1ffcc1bc541345c8829d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800333"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="da2d3-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="da2d3-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="da2d3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da2d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da2d3-105">自動的に解決された行から**emsabpUID**を取得し、**エントリ Id**を表示することを除いては、 [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)と同じ機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="da2d3-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da2d3-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="da2d3-106">Header file:</span></span>  <br/> |<span data-ttu-id="da2d3-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="da2d3-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="da2d3-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="da2d3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="da2d3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="da2d3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="da2d3-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="da2d3-110">Called by:</span></span>  <br/> |<span data-ttu-id="da2d3-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="da2d3-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="da2d3-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="da2d3-112">Parameters</span></span>

 <span data-ttu-id="da2d3-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="da2d3-113">_prwResolved_</span></span>
  
> <span data-ttu-id="da2d3-114">[in]**EmsabpUID**を取得し、**エントリ Id**を開くために使用される解決された行へのポインター。</span><span class="sxs-lookup"><span data-stu-id="da2d3-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="da2d3-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="da2d3-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="da2d3-116">[in]アドレス帳のエントリ id を開くために使用します。</span><span class="sxs-lookup"><span data-stu-id="da2d3-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="da2d3-117">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="da2d3-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="da2d3-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="da2d3-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="da2d3-119">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="da2d3-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="da2d3-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="da2d3-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="da2d3-121">[in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="da2d3-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="da2d3-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="da2d3-122">_lpInterface_</span></span>
  
> <span data-ttu-id="da2d3-123">[in][Open] エントリにアクセスするために使用されるインターフェイスのインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="da2d3-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="da2d3-124">NULL を渡すことは、標準的なオブジェクトのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="da2d3-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="da2d3-125">メッセージング ユーザーは、標準のインタ フェースは[IMailUser: IMAPIProp](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="da2d3-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="da2d3-126">配布リスト、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)は、コンテナー、および[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="da2d3-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="da2d3-127">呼び出し元は、適切な標準インターフェイスまたはインターフェイスの継承階層内に_lpInterface_を設定できます。</span><span class="sxs-lookup"><span data-stu-id="da2d3-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="da2d3-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="da2d3-128">_ulFlags_</span></span>
  
> <span data-ttu-id="da2d3-129">[in]エントリを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="da2d3-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="da2d3-130">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="da2d3-130">The following flags can be set:</span></span>
    
<span data-ttu-id="da2d3-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="da2d3-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="da2d3-132">最大許可されたネットワークとクライアントのアクセス許可を持つエントリを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="da2d3-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="da2d3-133">などの場合、クライアントでは、読み取りし、書き込みのアクセス許可、アドレス帳プロバイダーしようと読み取りでエントリを開き、書き込みのアクセス許可。</span><span class="sxs-lookup"><span data-stu-id="da2d3-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="da2d3-134">クライアントは、[open] エントリの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すと、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得するが許可されているアクセス レベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="da2d3-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="da2d3-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="da2d3-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="da2d3-136">オフライン アドレス帳のみを使用すると、名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="da2d3-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="da2d3-137">たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。</span><span class="sxs-lookup"><span data-stu-id="da2d3-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="da2d3-138">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="da2d3-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="da2d3-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="da2d3-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="da2d3-140">成功する可能性のあるエントリは、完全にオープンになり、エントリへの以降の呼び出しがエラーを返す可能性があることを示す前に呼び出しを使用できます。</span><span class="sxs-lookup"><span data-stu-id="da2d3-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="da2d3-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="da2d3-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="da2d3-142">GAL のみを使用すると、名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="da2d3-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="da2d3-143">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="da2d3-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="da2d3-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="da2d3-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="da2d3-145">エントリで開くことの要求は、アクセス許可を読み書きします。</span><span class="sxs-lookup"><span data-stu-id="da2d3-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="da2d3-146">エントリは読み取り専用アクセスで開くとき、既定であるために読み書き権限が与えられている MAPI_MODIFY が設定されているかどうかに関係なくクライアントを想定しません。</span><span class="sxs-lookup"><span data-stu-id="da2d3-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="da2d3-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="da2d3-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="da2d3-148">名前解決を実行するのには、オフライン アドレス帳を使用しません。</span><span class="sxs-lookup"><span data-stu-id="da2d3-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="da2d3-149">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="da2d3-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="da2d3-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="da2d3-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="da2d3-151">[out]開かれているエントリの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="da2d3-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="da2d3-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="da2d3-152">_lppUnk_</span></span>
  
> <span data-ttu-id="da2d3-153">[out]開かれているエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="da2d3-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

