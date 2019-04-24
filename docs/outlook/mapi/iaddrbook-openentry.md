---
title: iaddrbookopenentry
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287022"
---
# <a name="iaddrbookopenentry"></a><span data-ttu-id="d707d-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="d707d-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="d707d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d707d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d707d-105">アドレス帳エントリを開き、エントリへのアクセスに使用できるインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="d707d-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="d707d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d707d-106">Parameters</span></span>

<span data-ttu-id="d707d-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d707d-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="d707d-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="d707d-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="d707d-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="d707d-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="d707d-110">順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d707d-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="d707d-111">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="d707d-111">_lpInterface_</span></span>
  
> <span data-ttu-id="d707d-112">順番開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d707d-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="d707d-113">NULL を渡すと、オブジェクトの標準インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="d707d-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="d707d-114">メッセージングユーザーの場合、標準インターフェイスは[imailuser: imapiprop](imailuserimapiprop.md)です。</span><span class="sxs-lookup"><span data-stu-id="d707d-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="d707d-115">配布リストの場合、 [idistlist: IMAPIContainer](idistlistimapicontainer.md)およびコンテナーの場合は、 [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)になります。</span><span class="sxs-lookup"><span data-stu-id="d707d-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="d707d-116">呼び出し元は、 _lpinterface_を適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。</span><span class="sxs-lookup"><span data-stu-id="d707d-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="d707d-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d707d-117">_ulFlags_</span></span>
  
> <span data-ttu-id="d707d-118">順番エントリが開かれる方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d707d-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="d707d-119">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d707d-119">The following flags can be set.</span></span>
    
<span data-ttu-id="d707d-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d707d-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="d707d-121">許可された最大ネットワークおよびクライアントアクセス許可でエントリが開かれることを要求します。</span><span class="sxs-lookup"><span data-stu-id="d707d-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="d707d-122">たとえば、クライアントが読み取り/書き込みアクセス許可を持っている場合、アドレス帳プロバイダーは読み取り/書き込みアクセス許可でエントリを開こうとする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d707d-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="d707d-123">クライアントは、open エントリの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得することによって付与されたアクセスレベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="d707d-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="d707d-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="d707d-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="d707d-125">アドレス帳エントリを開き、キャッシュからのみアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d707d-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="d707d-126">たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d707d-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="d707d-127">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d707d-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="d707d-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d707d-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d707d-129">呼び出しが正常に終了し、エントリが完全に開かれて使用可能になる前に、エントリを後で呼び出すとエラーが返される可能性があることを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="d707d-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="d707d-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="d707d-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="d707d-131">名前解決を実行するには、GAL のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="d707d-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="d707d-132">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d707d-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="d707d-133">_ulflags_ MAPI_GAL_ONLY は、現在のダウンロード可能なヘッダーファイルでは定義されていない場合があります。その場合は、次の値を使用してコードに追加できます。 >`#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="d707d-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="d707d-134">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d707d-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="d707d-135">読み取り/書き込みアクセス許可を使用してエントリが開かれるように要求します。</span><span class="sxs-lookup"><span data-stu-id="d707d-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="d707d-136">既定では、エントリは読み取り専用アクセスで開かれるので、MAPI_MODIFY が設定されているかどうかに関係なく、クライアントは読み取り/書き込みアクセス許可が付与されたことを想定してはなりません。</span><span class="sxs-lookup"><span data-stu-id="d707d-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="d707d-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="d707d-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="d707d-138">オフラインアドレス帳を使用して名前解決を実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="d707d-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="d707d-139">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d707d-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="d707d-140">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="d707d-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="d707d-141">読み上げ開かれた項目の種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d707d-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="d707d-142">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="d707d-142">_lppUnk_</span></span>
  
> <span data-ttu-id="d707d-143">読み上げ開かれたエントリへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d707d-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d707d-144">戻り値</span><span class="sxs-lookup"><span data-stu-id="d707d-144">Return value</span></span>

<span data-ttu-id="d707d-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="d707d-145">S_OK</span></span> 
  
> <span data-ttu-id="d707d-146">エントリが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="d707d-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="d707d-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d707d-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d707d-148">ユーザーが十分なアクセス許可を持っていないエントリを開こうとしました。</span><span class="sxs-lookup"><span data-stu-id="d707d-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="d707d-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d707d-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d707d-150">_lな tryid_で表されるエントリは存在しません。</span><span class="sxs-lookup"><span data-stu-id="d707d-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="d707d-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d707d-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="d707d-152">_lな tryid_で指定されているエントリ識別子が認識されません。</span><span class="sxs-lookup"><span data-stu-id="d707d-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="d707d-153">この値は、対応するエントリを担当するアドレス帳プロバイダーが開かれていない場合に、通常返されます。</span><span class="sxs-lookup"><span data-stu-id="d707d-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d707d-154">解説</span><span class="sxs-lookup"><span data-stu-id="d707d-154">Remarks</span></span>

<span data-ttu-id="d707d-155">クライアントおよびサービスプロバイダーは、アドレス帳のエントリを開くために**IAddrBook:: openentry**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d707d-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="d707d-156">MAPI は、 _lMAPIUID tryid_パラメーターで渡されたエントリ識別子に含まれている[](mapiuid.md)構造に基づいて、適切なアドレス帳プロバイダーに呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="d707d-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="d707d-157">MAPI_MODIFY または MAPI_BEST_ACCESS フラグが設定されている場合を除いて、アドレス帳プロバイダー __ はエントリを読み取り専用として開きます。</span><span class="sxs-lookup"><span data-stu-id="d707d-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="d707d-158">ただし、これらのフラグは推奨事項です。</span><span class="sxs-lookup"><span data-stu-id="d707d-158">However, these flags are suggestions.</span></span> <span data-ttu-id="d707d-159">アドレス帳プロバイダーで、要求されたエントリの変更が許可されていない場合は、MAPI_E_NO_ACCESS が返されます。</span><span class="sxs-lookup"><span data-stu-id="d707d-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="d707d-160">_lpinterface_パラメーターは、開いているエントリへのアクセスに使用するインターフェイスを示します。</span><span class="sxs-lookup"><span data-stu-id="d707d-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="d707d-161">_lpinterface_で NULL を渡すことは、そのエントリの種類に対して標準の MAPI インターフェイスが使用されることを示します。</span><span class="sxs-lookup"><span data-stu-id="d707d-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="d707d-162">アドレス帳プロバイダーは_lpinterface_パラメーターで提案されたインターフェイスとは異なるインターフェイスを返す可能性があるため、発信者は_lpulobjtype_パラメーターで返された値を確認して、返されるオブジェクトの種類がどうかを判断する必要があります。予想される動作</span><span class="sxs-lookup"><span data-stu-id="d707d-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="d707d-163">オブジェクトの種類が想定された型ではない場合、呼び出し元は、 _lppunk_パラメーターをより適切な型にキャストできます。</span><span class="sxs-lookup"><span data-stu-id="d707d-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d707d-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="d707d-164">See also</span></span>

- [<span data-ttu-id="d707d-165">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d707d-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

