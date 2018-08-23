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
ms.openlocfilehash: 879ba4afe85e1f6db31bd829411689b2dad58ed9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565467"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="c5de1-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="c5de1-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="c5de1-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5de1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5de1-105">_PEmsmdbUID_パラメーターとして従来の**emsmdbUID**を使用する[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)と同じ機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="c5de1-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="c5de1-106">[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)への呼び出しの正しい**emsmdbUID**を取得することはできない場合に、この関数を使用しません。</span><span class="sxs-lookup"><span data-stu-id="c5de1-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5de1-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c5de1-107">Header file:</span></span>  <br/> |<span data-ttu-id="c5de1-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="c5de1-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="c5de1-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="c5de1-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="c5de1-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="c5de1-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="c5de1-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c5de1-111">Called by:</span></span>  <br/> |<span data-ttu-id="c5de1-112">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c5de1-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="c5de1-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c5de1-113">Parameters</span></span>

 <span data-ttu-id="c5de1-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="c5de1-114">_pmsess_</span></span>
  
> <span data-ttu-id="c5de1-115">[in]**IMAPISession**にログオンします。</span><span class="sxs-lookup"><span data-stu-id="c5de1-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="c5de1-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c5de1-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c5de1-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="c5de1-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="c5de1-118">[in]アドレス帳のエントリ id を開くために使用します。</span><span class="sxs-lookup"><span data-stu-id="c5de1-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="c5de1-119">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c5de1-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c5de1-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c5de1-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="c5de1-121">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="c5de1-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c5de1-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c5de1-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="c5de1-123">[in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c5de1-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="c5de1-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c5de1-124">_lpInterface_</span></span>
  
> <span data-ttu-id="c5de1-125">[in][Open] エントリにアクセスするために使用されるインターフェイスのインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c5de1-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="c5de1-126">NULL を渡すことは、標準的なオブジェクトのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="c5de1-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="c5de1-127">メッセージング ユーザーは、標準のインタ フェースは[IMailUser: IMAPIProp](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="c5de1-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="c5de1-128">配布リストには、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)とは、コンテナーの[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="c5de1-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="c5de1-129">呼び出し元は、適切な標準インターフェイスまたはインターフェイスの継承階層内に_lpInterface_を設定できます。</span><span class="sxs-lookup"><span data-stu-id="c5de1-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="c5de1-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c5de1-130">_ulFlags_</span></span>
  
> <span data-ttu-id="c5de1-131">[in]エントリを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="c5de1-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="c5de1-132">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c5de1-132">The following flags can be set:</span></span>
    
<span data-ttu-id="c5de1-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c5de1-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="c5de1-134">最大許可されたネットワークとクライアントのアクセス許可を持つエントリを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="c5de1-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="c5de1-135">などの場合、クライアントでは、読み取りし、書き込みのアクセス許可、アドレス帳プロバイダーしようと読み取りでエントリを開き、書き込みのアクセス許可。</span><span class="sxs-lookup"><span data-stu-id="c5de1-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="c5de1-136">クライアントは、[open] エントリの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すと、PR_ACCESS_LEVEL (PidTagAccessLevel) プロパティを取得するが許可されているアクセス レベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="c5de1-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="c5de1-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="c5de1-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="c5de1-138">オフライン アドレス帳のみを使用すると、名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="c5de1-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="c5de1-139">たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。</span><span class="sxs-lookup"><span data-stu-id="c5de1-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="c5de1-140">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="c5de1-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="c5de1-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c5de1-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="c5de1-142">成功する可能性のあるエントリは、完全にオープンになり、エントリへの以降の呼び出しがエラーを返す可能性があることを示す前に呼び出しを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c5de1-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="c5de1-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="c5de1-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="c5de1-144">GAL のみを使用すると、名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="c5de1-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="c5de1-145">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="c5de1-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="c5de1-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="c5de1-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="c5de1-147">エントリで開くことの要求は、アクセス許可を読み書きします。</span><span class="sxs-lookup"><span data-stu-id="c5de1-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="c5de1-148">エントリは読み取り専用アクセスで開くとき、既定であるために読み書き権限が与えられている MAPI_MODIFY が設定されているかどうかに関係なくクライアントを想定しません。</span><span class="sxs-lookup"><span data-stu-id="c5de1-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="c5de1-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="c5de1-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="c5de1-150">名前解決を実行するのには、オフライン アドレス帳を使用しません。</span><span class="sxs-lookup"><span data-stu-id="c5de1-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="c5de1-151">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="c5de1-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="c5de1-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="c5de1-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="c5de1-153">[out]開かれているエントリの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c5de1-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="c5de1-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="c5de1-154">_lppUnk_</span></span>
  
> <span data-ttu-id="c5de1-155">[out]開かれているエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c5de1-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

