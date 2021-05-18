---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 20344185ffcbd90017fa3c3493218bd9b3ddfd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408895"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="37e86-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="37e86-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="37e86-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37e86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37e86-105">_pEmsabpUID_ で識別Exchangeアドレス帳を使用して entryID を開きます。 </span><span class="sxs-lookup"><span data-stu-id="37e86-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="37e86-106">この関数は[IAddrBook::OpenEntry](iaddrbook-openentry.md)と同様に動作しますが、この関数を使用すると[、IAddrBook::OpenEntry](iaddrbook-openentry.md)が予期される Exchange アドレス帳プロバイダーを使用して開きます。</span><span class="sxs-lookup"><span data-stu-id="37e86-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37e86-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="37e86-107">Header file:</span></span>  <br/> |<span data-ttu-id="37e86-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="37e86-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="37e86-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="37e86-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="37e86-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="37e86-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="37e86-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="37e86-111">Called by:</span></span>  <br/> |<span data-ttu-id="37e86-112">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="37e86-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUID(
  const MAPIUID *pEmsabpUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="37e86-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37e86-113">Parameters</span></span>

 <span data-ttu-id="37e86-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="37e86-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="37e86-115">[in]この関数がエントリ識別子の詳細を表示するために使用する Exchange アドレス帳プロバイダーを含む Exchange サービスを識別する **emsmdbUID** へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37e86-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="37e86-116">受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出し[は IAddrBook::D etails](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="37e86-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="37e86-117">このパラメーターが NULL または 0 の MAPIUID の場合、この関数は [IAddrBook::D同様に動作します](iaddrbook-details.md)。</span><span class="sxs-lookup"><span data-stu-id="37e86-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="37e86-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="37e86-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="37e86-119">[in]エントリ識別子を開くのに使用するアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="37e86-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="37e86-120">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="37e86-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="37e86-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="37e86-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="37e86-122">[in]  _lpEntryID_ パラメーターで指定されたエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="37e86-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="37e86-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="37e86-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="37e86-124">[in]開くアドレス帳エントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37e86-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="37e86-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="37e86-125">_lpInterface_</span></span>
  
> <span data-ttu-id="37e86-126">[in]開いているエントリへのアクセスに使用されるインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37e86-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="37e86-127">NULL を渡す場合は、オブジェクトの標準インターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="37e86-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="37e86-128">メッセージング ユーザーの場合、標準インターフェイスは [IMailUser : IMAPIProp です](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="37e86-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="37e86-129">配布リストの場合 [、IDistList : IMAPIContainer](idistlistimapicontainer.md)であり、コンテナーの場合は [IABContainer : IMAPIContainer です](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="37e86-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="37e86-130">呼び出し元は  _、lpInterface を_ 適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。</span><span class="sxs-lookup"><span data-stu-id="37e86-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="37e86-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="37e86-131">_ulFlags_</span></span>
  
> <span data-ttu-id="37e86-132">[in]エントリの開き方を制御するフラグのビットマスクです。次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="37e86-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="37e86-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="37e86-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="37e86-134">許可されるネットワークおよびクライアントの最大アクセス許可を使用してエントリを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="37e86-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="37e86-135">たとえば、クライアントに読み取りおよび書き込みアクセス許可がある場合、アドレス帳プロバイダーは読み取りおよび書き込みアクセス許可を持つエントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="37e86-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="37e86-136">クライアントは、開いているエントリの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出し、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得することで、付与されたアクセス レベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="37e86-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="37e86-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="37e86-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="37e86-138">名前解決を実行するには、オフライン アドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="37e86-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="37e86-139">たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="37e86-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="37e86-140">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="37e86-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="37e86-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="37e86-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="37e86-142">エントリが完全に開いて使用可能になる前に、呼び出しが成功する可能性があります。その後のエントリへの呼び出しがエラーを返す可能性を示します。</span><span class="sxs-lookup"><span data-stu-id="37e86-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="37e86-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="37e86-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="37e86-144">名前解決を実行するには、GAL のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="37e86-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="37e86-145">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="37e86-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="37e86-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="37e86-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="37e86-147">読み取りおよび書き込みアクセス許可を持つエントリを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="37e86-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="37e86-148">既定では、読み取り専用アクセスでエントリが開くので、クライアントは、読み取りアクセス許可と書き込みアクセス許可が設定されているかどうかに関係なく、読み取りおよび書き込み権限が付与MAPI_MODIFY必要があります。</span><span class="sxs-lookup"><span data-stu-id="37e86-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="37e86-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="37e86-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="37e86-150">名前解決を実行するには、オフライン アドレス帳を使用しない。</span><span class="sxs-lookup"><span data-stu-id="37e86-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="37e86-151">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="37e86-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="37e86-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="37e86-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="37e86-153">[out]開いたエントリの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="37e86-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="37e86-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="37e86-154">_lppUnk_</span></span>
  
> <span data-ttu-id="37e86-155">[out]開いたエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37e86-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

