---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 20344185ffcbd90017fa3c3493218bd9b3ddfd74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347818"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="d3475-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="d3475-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="d3475-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3475-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3475-105">_pEmsabpUID_によって識別される Exchange アドレス帳を使用して、 **entryID**を開きます。</span><span class="sxs-lookup"><span data-stu-id="d3475-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="d3475-106">この関数は、 [IAddrBook:: openentry](iaddrbook-openentry.md)と同様に動作します。ただし、この関数を使用すると、予期される Exchange アドレス帳プロバイダーを使用して[IAddrBook:: openentry](iaddrbook-openentry.md)が開かれることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="d3475-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3475-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d3475-107">Header file:</span></span>  <br/> |<span data-ttu-id="d3475-108">abhelp .h</span><span class="sxs-lookup"><span data-stu-id="d3475-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="d3475-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="d3475-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="d3475-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="d3475-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="d3475-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d3475-111">Called by:</span></span>  <br/> |<span data-ttu-id="d3475-112">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="d3475-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d3475-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d3475-113">Parameters</span></span>

 <span data-ttu-id="d3475-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="d3475-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="d3475-115">順番この関数がエントリ識別子の詳細を表示するために使用する exchange アドレス帳プロバイダーを含む exchange サービスを識別する**emsmdbUID**へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d3475-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="d3475-116">受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出しは[IAddrBook::D etails](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="d3475-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="d3475-117">このパラメーターが NULL またはゼロ MAPIUID の場合、この関数は[IAddrBook::D etails](iaddrbook-details.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="d3475-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="d3475-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="d3475-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="d3475-119">順番エントリ識別子を開くために使用されるアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="d3475-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="d3475-120">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d3475-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d3475-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d3475-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="d3475-122">順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。</span><span class="sxs-lookup"><span data-stu-id="d3475-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d3475-123">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="d3475-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="d3475-124">順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d3475-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="d3475-125">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="d3475-125">_lpInterface_</span></span>
  
> <span data-ttu-id="d3475-126">順番開いているエントリへのアクセスに使用されるインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d3475-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="d3475-127">NULL を渡すと、オブジェクトの標準インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="d3475-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="d3475-128">メッセージングユーザーの場合、標準インターフェイスは[imailuser: imapiprop](imailuserimapiprop.md)です。</span><span class="sxs-lookup"><span data-stu-id="d3475-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="d3475-129">配布リストの場合、 [idistlist: IMAPIContainer](idistlistimapicontainer.md)およびコンテナーの場合は、 [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)になります。</span><span class="sxs-lookup"><span data-stu-id="d3475-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="d3475-130">呼び出し元は、 _lpinterface_を適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。</span><span class="sxs-lookup"><span data-stu-id="d3475-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="d3475-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d3475-131">_ulFlags_</span></span>
  
> <span data-ttu-id="d3475-132">順番エントリが開かれる方法を制御するフラグのビットマスク。次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d3475-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="d3475-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d3475-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="d3475-134">許可された最大ネットワークおよびクライアントアクセス許可でエントリが開かれることを要求します。</span><span class="sxs-lookup"><span data-stu-id="d3475-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="d3475-135">たとえば、クライアントが読み取りおよび書き込みアクセス許可を持っている場合、アドレス帳プロバイダーは、読み取りおよび書き込みアクセス許可を持つエントリを開こうとします。</span><span class="sxs-lookup"><span data-stu-id="d3475-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="d3475-136">クライアントは、開いているエントリの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得することによって付与されたアクセスレベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="d3475-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="d3475-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="d3475-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="d3475-138">名前解決を実行するには、オフラインアドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3475-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="d3475-139">たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d3475-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="d3475-140">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d3475-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="d3475-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d3475-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="d3475-142">呼び出しが正常に完了します。エントリが完全に開かれて使用可能になる前に、エントリへの以降の呼び出しでエラーが返される可能性があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="d3475-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="d3475-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="d3475-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="d3475-144">名前解決を実行するには、GAL のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3475-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="d3475-145">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d3475-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="d3475-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d3475-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="d3475-147">読み取りと書き込みのアクセス許可を使用して、エントリを開くように要求します。</span><span class="sxs-lookup"><span data-stu-id="d3475-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="d3475-148">既定では、エントリは読み取り専用アクセスで開かれるため、クライアントは、MAPI_MODIFY が設定されているかどうかに関係なく、読み取りおよび書き込みアクセス許可が付与されたことを想定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d3475-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="d3475-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="d3475-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="d3475-150">オフラインアドレス帳を使用して名前解決を実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="d3475-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="d3475-151">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d3475-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="d3475-152">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="d3475-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="d3475-153">読み上げ開かれた項目の種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d3475-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="d3475-154">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="d3475-154">_lppUnk_</span></span>
  
> <span data-ttu-id="d3475-155">読み上げ開かれたエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d3475-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

