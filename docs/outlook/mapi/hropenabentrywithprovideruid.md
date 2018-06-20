---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e33e656e70802437ab8b8717c5e175e2a13e384e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800303"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="2bc29-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="2bc29-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="2bc29-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2bc29-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2bc29-105">_PEmsabpUID_によって識別される、Exchange アドレス帳を使用して**エントリ Id**が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2bc29-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="2bc29-106">この関数は、この関数を使用すると、予想される Exchange アドレス帳プロバイダーを使用して[アドレス帳コンテナー](iaddrbook-openentry.md)が開かれていることを除いてに、[アドレス帳コンテナー](iaddrbook-openentry.md)同様に動作します。</span><span class="sxs-lookup"><span data-stu-id="2bc29-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2bc29-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2bc29-107">Header file:</span></span>  <br/> |<span data-ttu-id="2bc29-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="2bc29-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="2bc29-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="2bc29-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="2bc29-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="2bc29-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="2bc29-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2bc29-111">Called by:</span></span>  <br/> |<span data-ttu-id="2bc29-112">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="2bc29-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="2bc29-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="2bc29-113">Parameters</span></span>

 <span data-ttu-id="2bc29-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="2bc29-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="2bc29-115">[in]エントリ id の詳細を表示するのにはこの関数を使用する必要があります Exchange のアドレス帳プロバイダーが含まれている Exchange サービスを識別する**emsmdbUID**へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2bc29-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="2bc29-116">受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子でない場合は、このパラメーターは無視され、関数呼び出しは、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="2bc29-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="2bc29-117">このパラメーターが NULL またはゼロの MAPIUID の場合は、この関数は、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="2bc29-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="2bc29-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="2bc29-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="2bc29-119">[in]アドレス帳のエントリ id を開くために使用します。</span><span class="sxs-lookup"><span data-stu-id="2bc29-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="2bc29-120">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="2bc29-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="2bc29-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2bc29-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="2bc29-122">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="2bc29-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2bc29-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="2bc29-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="2bc29-124">[in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2bc29-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="2bc29-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="2bc29-125">_lpInterface_</span></span>
  
> <span data-ttu-id="2bc29-126">[in][Open] エントリにアクセスするために使用されるインターフェイスのインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2bc29-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="2bc29-127">NULL を渡すことは、標準的なオブジェクトのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="2bc29-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="2bc29-128">メッセージング ユーザーは、標準のインタ フェースは[IMailUser: IMAPIProp](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="2bc29-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="2bc29-129">配布リスト、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)は、コンテナー、および[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="2bc29-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="2bc29-130">呼び出し元は、適切な標準インターフェイスまたはインターフェイスの継承階層内に_lpInterface_を設定できます。</span><span class="sxs-lookup"><span data-stu-id="2bc29-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="2bc29-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2bc29-131">_ulFlags_</span></span>
  
> <span data-ttu-id="2bc29-132">[in]方法を制御するフラグのビットマスクのエントリを開いて、次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="2bc29-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="2bc29-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2bc29-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="2bc29-134">最大許可されたネットワークとクライアントのアクセス許可を持つエントリを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="2bc29-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="2bc29-135">などの場合、クライアントでは、読み取りし、書き込みのアクセス許可、アドレス帳プロバイダーしようと読み取りでエントリを開き、書き込みのアクセス許可。</span><span class="sxs-lookup"><span data-stu-id="2bc29-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="2bc29-136">クライアントは、[open] エントリの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すと、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得するが許可されているアクセス レベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="2bc29-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="2bc29-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="2bc29-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="2bc29-138">名前解決を実行するのにには、オフライン アドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="2bc29-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="2bc29-139">たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。</span><span class="sxs-lookup"><span data-stu-id="2bc29-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="2bc29-140">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="2bc29-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="2bc29-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="2bc29-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="2bc29-142">成功する可能性のあるエントリは、完全にオープンになり、エントリへの以降の呼び出しがエラーを返す可能性があることを示す前に呼び出しを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2bc29-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="2bc29-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="2bc29-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="2bc29-144">GAL のみを使用して、名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="2bc29-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="2bc29-145">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="2bc29-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="2bc29-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="2bc29-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="2bc29-147">エントリで開くことの要求は、アクセス許可を読み書きします。</span><span class="sxs-lookup"><span data-stu-id="2bc29-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="2bc29-148">エントリは読み取り専用アクセスで開くとき、既定であるために読み書き権限が与えられている MAPI_MODIFY が設定されているかどうかに関係なくクライアントを想定しません。</span><span class="sxs-lookup"><span data-stu-id="2bc29-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="2bc29-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="2bc29-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="2bc29-150">名前解決を実行するのには、オフライン アドレス帳を使用しません。</span><span class="sxs-lookup"><span data-stu-id="2bc29-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="2bc29-151">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="2bc29-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="2bc29-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="2bc29-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="2bc29-153">[out]開かれているエントリの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2bc29-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="2bc29-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="2bc29-154">_lppUnk_</span></span>
  
> <span data-ttu-id="2bc29-155">[out]開かれているエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2bc29-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

