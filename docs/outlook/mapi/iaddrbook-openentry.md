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
description: '�ŏI�X�V��: 2013�N2��1��'
ms.openlocfilehash: fa279962043f6f7cb7a134b624000c9c7e65369f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19800394"
---
# <a name="iaddrbookopenentry"></a><span data-ttu-id="8bced-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="8bced-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="8bced-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8bced-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8bced-105">アドレス帳エントリを開き、エントリにアクセスするために使用するインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="8bced-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="8bced-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8bced-106">Parameters</span></span>

<span data-ttu-id="8bced-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8bced-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="8bced-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="8bced-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="8bced-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8bced-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="8bced-110">[in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8bced-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="8bced-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8bced-111">_lpInterface_</span></span>
  
> <span data-ttu-id="8bced-112">[in][Open] エントリにアクセスするために使用するインターフェイスのインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8bced-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="8bced-113">NULL を渡すと、オブジェクトの標準的なインターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="8bced-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="8bced-114">メッセージング ユーザーは、標準のインタ フェースは[IMailUser: IMAPIProp](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="8bced-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="8bced-115">配布リスト、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)は、コンテナー、および[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="8bced-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="8bced-116">呼び出し元は、適切な標準インターフェイスまたはインターフェイスの継承階層内に_lpInterface_を設定できます。</span><span class="sxs-lookup"><span data-stu-id="8bced-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="8bced-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8bced-117">_ulFlags_</span></span>
  
> <span data-ttu-id="8bced-118">[in]エントリを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="8bced-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="8bced-119">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="8bced-119">The following flags can be set.</span></span>
    
<span data-ttu-id="8bced-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8bced-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="8bced-121">最大許可されたネットワークとクライアントのアクセス許可を持つエントリを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="8bced-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="8bced-122">たとえば、クライアントに読み取り/書き込み権限がある場合は、アドレス帳プロバイダーは、読み取り/書き込みアクセス許可を持つエントリを開くしようとします。</span><span class="sxs-lookup"><span data-stu-id="8bced-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="8bced-123">クライアントは、[open] エントリの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すと、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得するに与えられたアクセス レベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="8bced-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="8bced-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="8bced-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="8bced-125">アドレス帳エントリを開き、[キャッシュからのみアクセスすること。</span><span class="sxs-lookup"><span data-stu-id="8bced-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="8bced-126">たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。</span><span class="sxs-lookup"><span data-stu-id="8bced-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="8bced-127">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="8bced-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="8bced-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8bced-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8bced-129">成功する可能性のあるエントリは、完全にオープンになり、エントリへの以降の呼び出しがエラーを返す可能性があることを示す前に呼び出しを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8bced-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="8bced-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="8bced-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="8bced-131">GAL のみを使用して、名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="8bced-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="8bced-132">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="8bced-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="8bced-133">_UlFlags_ MAPI_GAL_ONLY は、現在あるダウンロード可能なヘッダー ファイルで定義されていない可能性があります、場合に追加できます、次の値を使用してコード: >`#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="8bced-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="8bced-134">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="8bced-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="8bced-135">エントリで開くことの要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="8bced-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="8bced-136">エントリは、既定で読み取り専用アクセスで開かれるが、ためクライアントを考慮に入れて MAPI_MODIFY が設定されているかどうかに関係なく読み取り/書き込み権限が与えられたことです。</span><span class="sxs-lookup"><span data-stu-id="8bced-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="8bced-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="8bced-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="8bced-138">名前解決を実行するのには、オフライン アドレス帳を使用しません。</span><span class="sxs-lookup"><span data-stu-id="8bced-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="8bced-139">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="8bced-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="8bced-140">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="8bced-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="8bced-141">[out]開かれているエントリの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8bced-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="8bced-142">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="8bced-142">_lppUnk_</span></span>
  
> <span data-ttu-id="8bced-143">[out]開かれているエントリへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8bced-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8bced-144">�߂�l</span><span class="sxs-lookup"><span data-stu-id="8bced-144">Return value</span></span>

<span data-ttu-id="8bced-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="8bced-145">S_OK</span></span> 
  
> <span data-ttu-id="8bced-146">エントリが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="8bced-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="8bced-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8bced-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8bced-148">ユーザーが十分なアクセス許可を持っているエントリを開くしようとしました。</span><span class="sxs-lookup"><span data-stu-id="8bced-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="8bced-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8bced-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8bced-150">_LpEntryID_によって表されるエントリが存在しません。</span><span class="sxs-lookup"><span data-stu-id="8bced-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="8bced-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8bced-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="8bced-152">_LpEntryID_で指定されたエントリの識別子を指定することはありません。</span><span class="sxs-lookup"><span data-stu-id="8bced-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="8bced-153">この値は通常、対応するエントリのアドレス帳プロバイダーが開いていない場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="8bced-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8bced-154">注釈</span><span class="sxs-lookup"><span data-stu-id="8bced-154">Remarks</span></span>

<span data-ttu-id="8bced-155">クライアントおよびサービス プロバイダーを開くには、アドレス帳のエントリの**アドレス帳コンテナー**のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8bced-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="8bced-156">MAPI では、 _lpEntryID_パラメーターで渡されたエントリの識別子に含まれる[MAPIUID](mapiuid.md)構造に基づく、適切なアドレス帳プロバイダーへの呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="8bced-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="8bced-157">_UlFlags_パラメーターで MAPI_MODIFY または MAPI_BEST_ACCESS フラグが設定されていない場合、アドレス帳プロバイダーには読み取り専用でエントリが開きます。</span><span class="sxs-lookup"><span data-stu-id="8bced-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="8bced-158">ただし、これらのフラグは、ご提案します。</span><span class="sxs-lookup"><span data-stu-id="8bced-158">However, these flags are suggestions.</span></span> <span data-ttu-id="8bced-159">アドレス帳プロバイダーが要求されたエントリの変更を許可していない場合は、MAPI_E_NO_ACCESS を返します。</span><span class="sxs-lookup"><span data-stu-id="8bced-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="8bced-160">_LpInterface_パラメーターでは、開かれているエントリにアクセスするのにはどのインタ フェースを使用する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="8bced-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="8bced-161">_LpInterface_に NULL を渡すことを示すエントリの種類の標準的な MAPI インターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bced-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="8bced-162">呼び出し側に返されるオブジェクトの型があるかどうかを判断するのには_lpulObjType_パラメーターで返される値をチェックする必要があるため、アドレス帳プロバイダーは、 _lpInterface_パラメーターによって示されたものとは別のインターフェイスを返すことがあります、何が必要です。</span><span class="sxs-lookup"><span data-stu-id="8bced-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="8bced-163">型のオブジェクトの種類がない場合は、呼び出し元は_lppUnk_パラメーターより適切な型にキャストできます。</span><span class="sxs-lookup"><span data-stu-id="8bced-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8bced-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="8bced-164">See also</span></span>

- [<span data-ttu-id="8bced-165">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8bced-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

