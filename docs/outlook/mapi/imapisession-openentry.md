---
title: imapisessionopenentry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329415"
---
# <a name="imapisessionopenentry"></a><span data-ttu-id="2a34a-103">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="2a34a-103">IMAPISession::OpenEntry</span></span>

  
  
<span data-ttu-id="2a34a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a34a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a34a-105">オブジェクトを開き、追加のアクセスのためのインターフェイスポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-105">Opens an object and returns an interface pointer for additional access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2a34a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2a34a-106">Parameters</span></span>

 <span data-ttu-id="2a34a-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2a34a-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="2a34a-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="2a34a-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2a34a-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="2a34a-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="2a34a-110">順番開くオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2a34a-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="2a34a-111">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="2a34a-111">_lpInterface_</span></span>
  
> <span data-ttu-id="2a34a-112">順番開いているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2a34a-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="2a34a-113">NULL を渡すと、オブジェクトの標準インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="2a34a-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="2a34a-114">たとえば、開くオブジェクトがメッセージの場合、標準インターフェイスは[IMessage](imessageimapiprop.md)になります。フォルダーの場合は、 [imapifolder](imapifolderimapicontainer.md)です。</span><span class="sxs-lookup"><span data-stu-id="2a34a-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="2a34a-115">アドレス帳オブジェクトの標準インターフェイスは、配布リストの[idistlist](idistlistimapicontainer.md)で、メッセージングユーザーの[idistlist](imailuserimapiprop.md)です。</span><span class="sxs-lookup"><span data-stu-id="2a34a-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="2a34a-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2a34a-116">_ulFlags_</span></span>
  
> <span data-ttu-id="2a34a-117">順番オブジェクトを開く方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2a34a-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="2a34a-118">次のフラグを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a34a-118">The following flags can be used:</span></span>
    
<span data-ttu-id="2a34a-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2a34a-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="2a34a-120">ユーザーに対して許可されている最大のネットワークアクセス許可、およびクライアントアプリケーションの最大アクセスを使用して、オブジェクトを開くように要求します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-120">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="2a34a-121">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、読み取り/書き込みアクセス許可を使用してオブジェクトを開く必要があります。クライアントが読み取り専用アクセス許可を持っている場合、そのオブジェクトは読み取り専用アクセス許可で開かれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a34a-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span> 
    
<span data-ttu-id="2a34a-122">MAPI_CACHE_OK</span><span class="sxs-lookup"><span data-stu-id="2a34a-122">MAPI_CACHE_OK</span></span>
  
> <span data-ttu-id="2a34a-123">オフラインアドレス帳を含むすべての方法を使用して、名前の解決を行います。</span><span class="sxs-lookup"><span data-stu-id="2a34a-123">Use all means, including offline address books, to perform name resolution.</span></span>
    
<span data-ttu-id="2a34a-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="2a34a-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="2a34a-125">名前解決を実行するには、オフラインアドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-125">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="2a34a-126">たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="2a34a-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="2a34a-127">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="2a34a-127">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="2a34a-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="2a34a-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="2a34a-129">呼び出し元のクライアントがオブジェクトを完全に使用できるようになる前に、 **openentry**が正常に返されることを許可します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-129">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="2a34a-130">オブジェクトが使用できない場合は、その後のオブジェクト呼び出しでエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="2a34a-130">If the object is not available, making a subsequent object call can cause an error.</span></span> 
    
<span data-ttu-id="2a34a-131">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="2a34a-131">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="2a34a-132">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-132">Requests read/write permission.</span></span> <span data-ttu-id="2a34a-133">既定では、オブジェクトは読み取り専用のアクセス許可で開かれ、読み取り/書き込みアクセス許可が付与されているという前提でクライアントを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="2a34a-133">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
<span data-ttu-id="2a34a-134">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="2a34a-134">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="2a34a-135">オフラインアドレス帳を使用して名前解決を実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="2a34a-135">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="2a34a-136">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="2a34a-136">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="2a34a-137">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="2a34a-137">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="2a34a-138">現在、削除済みアイテムの保存期間内にあるとマークされているアイテムを表示します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-138">Show items that are currently marked as soft deleted (that is, they are in the deleted item retention time phase).</span></span>
    
 <span data-ttu-id="2a34a-139">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="2a34a-139">_lpulObjType_</span></span>
  
> <span data-ttu-id="2a34a-140">読み上げ開かれているオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2a34a-140">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="2a34a-141">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="2a34a-141">_lppUnk_</span></span>
  
> <span data-ttu-id="2a34a-142">読み上げ開かれているオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2a34a-142">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2a34a-143">戻り値</span><span class="sxs-lookup"><span data-stu-id="2a34a-143">Return value</span></span>

<span data-ttu-id="2a34a-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="2a34a-144">S_OK</span></span> 
  
> <span data-ttu-id="2a34a-145">オブジェクトが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="2a34a-145">The object was opened successfully.</span></span>
    
<span data-ttu-id="2a34a-146">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2a34a-146">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="2a34a-147">読み取り専用オブジェクトを変更しようとしました。または、ユーザーが十分な権限を持っていないオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="2a34a-147">An attempt was made to modify a read-only object or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="2a34a-148">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2a34a-148">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2a34a-149">_lな tryid_パラメーターに渡されたエントリ id に関連付けられたオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="2a34a-149">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="2a34a-150">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2a34a-150">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="2a34a-151">_lな tryid_パラメーターで渡されたエントリ id は、認識できない形式です。</span><span class="sxs-lookup"><span data-stu-id="2a34a-151">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="2a34a-152">通常、この値は、オブジェクトを含むサービスプロバイダーが開かれていない場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="2a34a-152">This value is typically returned if the service provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2a34a-153">解説</span><span class="sxs-lookup"><span data-stu-id="2a34a-153">Remarks</span></span>

<span data-ttu-id="2a34a-154">**imapisession:: openentry**メソッドは、メッセージストアまたはアドレス帳オブジェクトを開き、オブジェクトへのアクセスに使用できるインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-154">The **IMAPISession::OpenEntry** method opens a message store or address book object, returning a pointer to an interface that can be used to access the object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2a34a-155">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2a34a-155">Notes to callers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a34a-156">フォルダーやメッセージなどのパブリックストアでフォルダーエントリを開くときは、 **imapisession:: openentry**の代わりに[IMsgStore:: openentry](imsgstore-openentry.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-156">When opening folder entries on a public store, such as folders and messages, use [IMsgStore::OpenEntry](imsgstore-openentry.md) instead of **IMAPISession::OpenEntry**.</span></span> <span data-ttu-id="2a34a-157">これにより、プロファイルに複数の Exchange アカウントが定義されている場合に、パブリックフォルダーが正しく機能することが保証されます。</span><span class="sxs-lookup"><span data-stu-id="2a34a-157">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
<span data-ttu-id="2a34a-158">開くオブジェクトの種類がわからない場合にのみ、 **imapisession:: openentry**のみを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-158">Call **IMAPISession::OpenEntry** only when you do not know what kind of object that you are opening.</span></span> <span data-ttu-id="2a34a-159">フォルダーまたはメッセージを開こうとしていることがわかっている場合は、 [IMsgStore:: openentry](imsgstore-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-159">If you know that you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="2a34a-160">アドレス帳コンテナー、メッセージングユーザー、または配布リストを開いていることがわかっている場合は、 [IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-160">If you know that you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="2a34a-161">これらのより具体的な方法は、 **imapisession:: openentry**よりも高速です。</span><span class="sxs-lookup"><span data-stu-id="2a34a-161">These more specific methods are faster than **IMAPISession::OpenEntry**.</span></span> 
  
<span data-ttu-id="2a34a-162">MAPI では、 _ulflags_パラメーターに MAPI_MODIFY または MAPI_BEST_ACCESS フラグを設定しない限り、読み取り専用アクセス許可を持つすべてのオブジェクトが開かれます。</span><span class="sxs-lookup"><span data-stu-id="2a34a-162">MAPI opens all objects with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="2a34a-163">これらのフラグのいずれかを設定しても、特定の種類のアクセス権は保証されません。付与されるアクセス許可は、サービスプロバイダー、アクセスレベル、およびオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="2a34a-163">Setting one of these flags does not guarantee a particular type of access; the permissions that are granted depend on the service provider, the access level, and the object.</span></span> <span data-ttu-id="2a34a-164">開いているオブジェクトのアクセスレベルを確認するには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-164">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="2a34a-165">**imapisession:: openentry**を呼び出し、メッセージストアのエントリ識別子をポイントするように_lMDB_NO_DIALOG tryid_を設定することは、 [imapisession:: openmsgstore](imapisession-openmsgstore.md)メソッドをフラグセットを指定して呼び出すのと同じです。</span><span class="sxs-lookup"><span data-stu-id="2a34a-165">Calling **IMAPISession::OpenEntry** and setting  _lpEntryID_ to point to the entry identifier of a message store is the same as calling the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method with the MDB_NO_DIALOG flag set.</span></span> <span data-ttu-id="2a34a-166">フラグの設定も同様ですが、 **openmsgstore**で読み取り/書き込みアクセス許可を要求する場合は、MAPI_MODIFY ではなく MDB_WRITE フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a34a-166">The flag settings are also equivalent, except that to request read/write permission with **OpenMsgStore**, you must set the MDB_WRITE flag instead of MAPI_MODIFY.</span></span> 
  
<span data-ttu-id="2a34a-167">_lpulobjtype_パラメーターで返された値を調べて、返されたオブジェクトの種類が期待したものであるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2a34a-167">Check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what you expected.</span></span> <span data-ttu-id="2a34a-168">オブジェクトの種類が想定した型ではない場合は、ポインターを_lppunk_パラメーターから適切な型のポインターにキャストします。</span><span class="sxs-lookup"><span data-stu-id="2a34a-168">If the object type is not the type that you expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="2a34a-169">たとえば、フォルダーを開いている場合は、LPMAPIFOLDER 型のポインターに_lppunk_をキャストします。</span><span class="sxs-lookup"><span data-stu-id="2a34a-169">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2a34a-170">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="2a34a-170">MFCMAPI reference</span></span>

<span data-ttu-id="2a34a-171">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a34a-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2a34a-172">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="2a34a-172">**File**</span></span>|<span data-ttu-id="2a34a-173">**関数**</span><span class="sxs-lookup"><span data-stu-id="2a34a-173">**Function**</span></span>|<span data-ttu-id="2a34a-174">**コメント**</span><span class="sxs-lookup"><span data-stu-id="2a34a-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2a34a-175">MAPIFunctions</span><span class="sxs-lookup"><span data-stu-id="2a34a-175">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2a34a-176">callopenentry</span><span class="sxs-lookup"><span data-stu-id="2a34a-176">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="2a34a-177">mfcmapi は、 **imapisession:: openentry**メソッドを使用してオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="2a34a-177">MFCMAPI uses the **IMAPISession::OpenEntry** method to open an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a34a-178">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a34a-178">See also</span></span>



[<span data-ttu-id="2a34a-179">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="2a34a-179">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="2a34a-180">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="2a34a-180">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md)
  
[<span data-ttu-id="2a34a-181">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2a34a-181">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)
  
[<span data-ttu-id="2a34a-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="2a34a-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="2a34a-183">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="2a34a-183">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="2a34a-184">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2a34a-184">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="2a34a-185">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="2a34a-185">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="2a34a-186">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2a34a-186">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="2a34a-187">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2a34a-187">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

