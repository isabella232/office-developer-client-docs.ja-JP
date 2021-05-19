---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: '最終更新日: 2013 年 2 月 1 日'
ms.openlocfilehash: 293fe5a65c760f61ab0073e0eafc1a606c69050f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434166"
---
# <a name="iaddrbookopenentry"></a><span data-ttu-id="6fc98-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6fc98-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="6fc98-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fc98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fc98-105">アドレス帳エントリを開き、エントリへのアクセスに使用できるインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="6fc98-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="6fc98-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6fc98-106">Parameters</span></span>

<span data-ttu-id="6fc98-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6fc98-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="6fc98-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="6fc98-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="6fc98-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6fc98-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="6fc98-110">[in]開くアドレス帳エントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6fc98-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="6fc98-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6fc98-111">_lpInterface_</span></span>
  
> <span data-ttu-id="6fc98-112">[in]開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6fc98-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="6fc98-113">NULL を渡す場合、オブジェクトの標準インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="6fc98-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="6fc98-114">メッセージング ユーザーの場合、標準インターフェイスは [IMailUser : IMAPIProp です](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="6fc98-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="6fc98-115">配布リストの場合 [、IDistList : IMAPIContainer](idistlistimapicontainer.md) であり、コンテナーの場合は [IABContainer : IMAPIContainer です](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="6fc98-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="6fc98-116">呼び出し元は  _、lpInterface を_ 適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。</span><span class="sxs-lookup"><span data-stu-id="6fc98-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="6fc98-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6fc98-117">_ulFlags_</span></span>
  
> <span data-ttu-id="6fc98-118">[in]エントリの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="6fc98-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="6fc98-119">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6fc98-119">The following flags can be set.</span></span>
    
<span data-ttu-id="6fc98-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6fc98-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="6fc98-121">許可されるネットワークおよびクライアントの最大アクセス許可を使用してエントリを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="6fc98-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="6fc98-122">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合、アドレス帳プロバイダーは読み取り/書き込みアクセス許可を持つエントリを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fc98-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="6fc98-123">クライアントは、開いているエントリの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出し **、PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得することで、付与されたアクセス レベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="6fc98-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="6fc98-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="6fc98-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="6fc98-125">アドレス帳エントリを開き、キャッシュからのみアクセスします。</span><span class="sxs-lookup"><span data-stu-id="6fc98-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="6fc98-126">たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6fc98-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="6fc98-127">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6fc98-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="6fc98-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6fc98-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="6fc98-129">エントリが完全に開いて使用可能になる前に、呼び出しが成功する可能性があります。後でエントリを呼び出してもエラーが返される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6fc98-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="6fc98-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="6fc98-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="6fc98-131">名前解決を実行するには、GAL のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="6fc98-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="6fc98-132">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6fc98-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="6fc98-133">_ulFlags_ MAPI_GAL_ONLYは、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は、次の値を使用してコードに追加>`#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="6fc98-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="6fc98-134">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6fc98-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="6fc98-135">読み取り/書き込みアクセス許可を持つエントリを開く要求。</span><span class="sxs-lookup"><span data-stu-id="6fc98-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="6fc98-136">既定では、読み取り専用アクセスでエントリが開くので、クライアントは、読み取り/書き込みアクセス許可が設定されているかどうかに関係なく、読み取り/書き込み権限が付与MAPI_MODIFY必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fc98-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="6fc98-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="6fc98-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="6fc98-138">名前解決を実行するには、オフライン アドレス帳を使用しない。</span><span class="sxs-lookup"><span data-stu-id="6fc98-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="6fc98-139">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6fc98-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="6fc98-140">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="6fc98-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="6fc98-141">[out]開いたエントリの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6fc98-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="6fc98-142">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="6fc98-142">_lppUnk_</span></span>
  
> <span data-ttu-id="6fc98-143">[out]開いたエントリへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="6fc98-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6fc98-144">戻り値</span><span class="sxs-lookup"><span data-stu-id="6fc98-144">Return value</span></span>

<span data-ttu-id="6fc98-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="6fc98-145">S_OK</span></span> 
  
> <span data-ttu-id="6fc98-146">エントリが正常に開かされました。</span><span class="sxs-lookup"><span data-stu-id="6fc98-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="6fc98-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6fc98-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6fc98-148">ユーザーのアクセス許可が不十分なエントリを開く試みがあった。</span><span class="sxs-lookup"><span data-stu-id="6fc98-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="6fc98-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6fc98-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6fc98-150">_lpEntryID で表されるエントリ_ が存在しません。</span><span class="sxs-lookup"><span data-stu-id="6fc98-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="6fc98-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6fc98-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="6fc98-152">_lpEntryID で指定されたエントリ識別子_ は認識されません。</span><span class="sxs-lookup"><span data-stu-id="6fc98-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="6fc98-153">通常、この値は、対応するエントリを担当するアドレス帳プロバイダーが開いていない場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="6fc98-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6fc98-154">注釈</span><span class="sxs-lookup"><span data-stu-id="6fc98-154">Remarks</span></span>

<span data-ttu-id="6fc98-155">クライアントとサービス プロバイダーは **、IAddrBook::OpenEntry** メソッドを呼び出してアドレス帳エントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="6fc98-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="6fc98-156">MAPI は _、lpEntryID_ パラメーターで渡されたエントリ識別子に含まれる [MAPIUID](mapiuid.md)構造に基づいて、適切なアドレス帳プロバイダーに呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="6fc98-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="6fc98-157">アドレス帳プロバイダーは  _、ulFlags_ パラメーターの MAPI_MODIFYまたは MAPI_BEST_ACCESSフラグが設定されていない限り、読み取り専用としてエントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="6fc98-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="6fc98-158">ただし、これらのフラグは提案です。</span><span class="sxs-lookup"><span data-stu-id="6fc98-158">However, these flags are suggestions.</span></span> <span data-ttu-id="6fc98-159">アドレス帳プロバイダーが要求されたエントリの変更を許可しない場合は、アドレス帳プロバイダーはMAPI_E_NO_ACCESS。</span><span class="sxs-lookup"><span data-stu-id="6fc98-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="6fc98-160">_lpInterface パラメーター_ は、開かれたエントリにアクセスするために使用するインターフェイスを示します。</span><span class="sxs-lookup"><span data-stu-id="6fc98-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="6fc98-161">_lpInterface で NULL を渡す_ 場合は、その種類のエントリの標準 MAPI インターフェイスを使用する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="6fc98-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="6fc98-162">アドレス帳プロバイダーは  _、lpInterface_ パラメーターによって提案されたインターフェイスとは異なるインターフェイスを返す可能性があるため、呼び出し元は  _lpulObjType_ パラメーターで返された値を確認して、返されるオブジェクトの種類が予期した値であるかどうかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fc98-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="6fc98-163">オブジェクトの種類が予期される型ではない場合、呼び出し元は  _lppUnk_ パラメーターを、より適切な型にキャストできます。</span><span class="sxs-lookup"><span data-stu-id="6fc98-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6fc98-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="6fc98-164">See also</span></span>

- [<span data-ttu-id="6fc98-165">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6fc98-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

