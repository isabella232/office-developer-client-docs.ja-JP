---
title: IMAPISessionOpenEntry
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426388"
---
# <a name="imapisessionopenentry"></a><span data-ttu-id="be5c9-103">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="be5c9-103">IMAPISession::OpenEntry</span></span>

  
  
<span data-ttu-id="be5c9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be5c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be5c9-105">オブジェクトを開き、追加のアクセス用のインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="be5c9-105">Opens an object and returns an interface pointer for additional access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="be5c9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="be5c9-106">Parameters</span></span>

 <span data-ttu-id="be5c9-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="be5c9-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="be5c9-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="be5c9-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="be5c9-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="be5c9-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="be5c9-110">[in]開くオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be5c9-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="be5c9-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="be5c9-111">_lpInterface_</span></span>
  
> <span data-ttu-id="be5c9-112">[in]開いたオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be5c9-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="be5c9-113">NULL を渡す場合、オブジェクトの標準インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="be5c9-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="be5c9-114">たとえば、開くオブジェクトがメッセージの場合、標準インターフェイスは [IMessage です](imessageimapiprop.md)。フォルダーの場合 [、IMAPIFolder です](imapifolderimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="be5c9-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="be5c9-115">アドレス帳オブジェクトの標準インターフェイスは、 [配布リストの IDistList、](idistlistimapicontainer.md) メッセージング ユーザー [の IMailUser](imailuserimapiprop.md) です。</span><span class="sxs-lookup"><span data-stu-id="be5c9-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="be5c9-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be5c9-116">_ulFlags_</span></span>
  
> <span data-ttu-id="be5c9-117">[in]オブジェクトの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="be5c9-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="be5c9-118">次のフラグを使用できます。</span><span class="sxs-lookup"><span data-stu-id="be5c9-118">The following flags can be used:</span></span>
    
<span data-ttu-id="be5c9-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="be5c9-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="be5c9-120">ユーザーに許可される最大ネットワークアクセス許可と最大クライアント アプリケーション アクセスを使用してオブジェクトを開く要求。</span><span class="sxs-lookup"><span data-stu-id="be5c9-120">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="be5c9-121">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、オブジェクトを読み取り/書き込みアクセス許可で開く必要があります。クライアントに読み取り専用のアクセス許可がある場合は、オブジェクトを読み取り専用のアクセス許可で開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="be5c9-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span> 
    
<span data-ttu-id="be5c9-122">MAPI_CACHE_OK</span><span class="sxs-lookup"><span data-stu-id="be5c9-122">MAPI_CACHE_OK</span></span>
  
> <span data-ttu-id="be5c9-123">名前解決を実行するには、オフライン アドレス帳を含むすべての手段を使用します。</span><span class="sxs-lookup"><span data-stu-id="be5c9-123">Use all means, including offline address books, to perform name resolution.</span></span>
    
<span data-ttu-id="be5c9-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="be5c9-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="be5c9-125">名前解決を実行するには、オフライン アドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="be5c9-125">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="be5c9-126">たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="be5c9-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="be5c9-127">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="be5c9-127">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="be5c9-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="be5c9-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="be5c9-129">オブジェクトが呼び出し元のクライアントで完全に利用できる前に **、OpenEntry** が正常に返されるのを許可します。</span><span class="sxs-lookup"><span data-stu-id="be5c9-129">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="be5c9-130">オブジェクトが使用できない場合は、後続のオブジェクト呼び出しを実行するとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="be5c9-130">If the object is not available, making a subsequent object call can cause an error.</span></span> 
    
<span data-ttu-id="be5c9-131">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="be5c9-131">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="be5c9-132">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="be5c9-132">Requests read/write permission.</span></span> <span data-ttu-id="be5c9-133">既定では、オブジェクトは読み取り専用のアクセス許可で開き、クライアントは読み取り/書き込みアクセス許可が付与されるという前提で動作しません。</span><span class="sxs-lookup"><span data-stu-id="be5c9-133">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
<span data-ttu-id="be5c9-134">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="be5c9-134">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="be5c9-135">名前解決を実行するには、オフライン アドレス帳を使用しない。</span><span class="sxs-lookup"><span data-stu-id="be5c9-135">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="be5c9-136">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="be5c9-136">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="be5c9-137">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="be5c9-137">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="be5c9-138">現在、ソフト削除済みとしてマークされているアイテム (つまり、削除済みアイテムの保持時間フェーズにある) を表示します。</span><span class="sxs-lookup"><span data-stu-id="be5c9-138">Show items that are currently marked as soft deleted (that is, they are in the deleted item retention time phase).</span></span>
    
 <span data-ttu-id="be5c9-139">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="be5c9-139">_lpulObjType_</span></span>
  
> <span data-ttu-id="be5c9-140">[out]開いたオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be5c9-140">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="be5c9-141">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="be5c9-141">_lppUnk_</span></span>
  
> <span data-ttu-id="be5c9-142">[out]開いたオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="be5c9-142">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="be5c9-143">戻り値</span><span class="sxs-lookup"><span data-stu-id="be5c9-143">Return value</span></span>

<span data-ttu-id="be5c9-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="be5c9-144">S_OK</span></span> 
  
> <span data-ttu-id="be5c9-145">オブジェクトが正常に開かされました。</span><span class="sxs-lookup"><span data-stu-id="be5c9-145">The object was opened successfully.</span></span>
    
<span data-ttu-id="be5c9-146">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="be5c9-146">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="be5c9-147">読み取り専用オブジェクトを変更しようとしたか、ユーザーが不十分なアクセス許可を持つオブジェクトにアクセスしようとした。</span><span class="sxs-lookup"><span data-stu-id="be5c9-147">An attempt was made to modify a read-only object or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="be5c9-148">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="be5c9-148">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="be5c9-149">lpEntryID パラメーターで渡されたエントリ識別子に関連  _付けられたオブジェクトは含_ めではありません。</span><span class="sxs-lookup"><span data-stu-id="be5c9-149">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="be5c9-150">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="be5c9-150">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="be5c9-151">_lpEntryID_ パラメーターで渡されるエントリ識別子は、認識できない形式です。</span><span class="sxs-lookup"><span data-stu-id="be5c9-151">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="be5c9-152">通常、この値は、オブジェクトを含むサービス プロバイダーが開いていない場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="be5c9-152">This value is typically returned if the service provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="be5c9-153">注釈</span><span class="sxs-lookup"><span data-stu-id="be5c9-153">Remarks</span></span>

<span data-ttu-id="be5c9-154">**IMAPISession::OpenEntry** メソッドは、メッセージ ストアまたはアドレス帳オブジェクトを開き、オブジェクトへのアクセスに使用できるインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="be5c9-154">The **IMAPISession::OpenEntry** method opens a message store or address book object, returning a pointer to an interface that can be used to access the object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="be5c9-155">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="be5c9-155">Notes to callers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be5c9-156">フォルダーやメッセージなどのパブリック ストアでフォルダー エントリを開く場合は **、IMAPISession::OpenEntry** の代わりに [IMsgStore::OpenEntry](imsgstore-openentry.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="be5c9-156">When opening folder entries on a public store, such as folders and messages, use [IMsgStore::OpenEntry](imsgstore-openentry.md) instead of **IMAPISession::OpenEntry**.</span></span> <span data-ttu-id="be5c9-157">これにより、複数のアカウントがプロファイルで定義されている場合Exchangeパブリック フォルダーが正しく機能します。</span><span class="sxs-lookup"><span data-stu-id="be5c9-157">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
<span data-ttu-id="be5c9-158">**IMAPISession::OpenEntry** を呼び出すのは、開いているオブジェクトの種類が分からない場合のみです。</span><span class="sxs-lookup"><span data-stu-id="be5c9-158">Call **IMAPISession::OpenEntry** only when you do not know what kind of object that you are opening.</span></span> <span data-ttu-id="be5c9-159">フォルダーまたはメッセージを開いている場合は [、IMsgStore::OpenEntry を呼び出します](imsgstore-openentry.md)。</span><span class="sxs-lookup"><span data-stu-id="be5c9-159">If you know that you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="be5c9-160">アドレス帳コンテナー、メッセージング ユーザー、または配布リストを開いている場合は [、IAddrBook::OpenEntry を呼び出します](iaddrbook-openentry.md)。</span><span class="sxs-lookup"><span data-stu-id="be5c9-160">If you know that you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="be5c9-161">これらのより具体的なメソッドは **、IMAPISession::OpenEntry よりも高速です**。</span><span class="sxs-lookup"><span data-stu-id="be5c9-161">These more specific methods are faster than **IMAPISession::OpenEntry**.</span></span> 
  
<span data-ttu-id="be5c9-162">MAPI は  _、ulFlags_ パラメーターで MAPI_MODIFYまたはMAPI_BEST_ACCESSを設定しない限り、読み取り専用のアクセス許可を持つすべてのオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="be5c9-162">MAPI opens all objects with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="be5c9-163">これらのフラグのいずれかを設定しても、特定の種類のアクセスが保証されるという保証はありません。付与されるアクセス許可は、サービス プロバイダー、アクセス レベル、およびオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="be5c9-163">Setting one of these flags does not guarantee a particular type of access; the permissions that are granted depend on the service provider, the access level, and the object.</span></span> <span data-ttu-id="be5c9-164">開いたオブジェクトのアクセス レベルを確認するには、そのオブジェクト [(PidTagAccessLevel)](pidtagaccesslevel-canonical-property.md) **PR_ACCESS_LEVELプロパティを** 取得します。</span><span class="sxs-lookup"><span data-stu-id="be5c9-164">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="be5c9-165">**IMAPISession::OpenEntry** を呼び出し _、lpEntryID_ をメッセージ ストアのエントリ識別子をポイントする設定は、MDB_NO_DIALOG フラグセットを使用して [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドを呼び出すのと同じです。</span><span class="sxs-lookup"><span data-stu-id="be5c9-165">Calling **IMAPISession::OpenEntry** and setting  _lpEntryID_ to point to the entry identifier of a message store is the same as calling the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method with the MDB_NO_DIALOG flag set.</span></span> <span data-ttu-id="be5c9-166">また **、OpenMsgStore** で読み取り/書き込みアクセス許可を要求する場合を除き、フラグの設定も同じですが、MDB_WRITE フラグを設定する必要MAPI_MODIFY。</span><span class="sxs-lookup"><span data-stu-id="be5c9-166">The flag settings are also equivalent, except that to request read/write permission with **OpenMsgStore**, you must set the MDB_WRITE flag instead of MAPI_MODIFY.</span></span> 
  
<span data-ttu-id="be5c9-167">_lpulObjType_ パラメーターで返される値を確認して、返されるオブジェクトの種類が予期した値であるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="be5c9-167">Check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what you expected.</span></span> <span data-ttu-id="be5c9-168">オブジェクトの種類が予期した型ではない場合は  _、lppUnk_ パラメーターから適切な型のポインターにポインターをキャストします。</span><span class="sxs-lookup"><span data-stu-id="be5c9-168">If the object type is not the type that you expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="be5c9-169">たとえば、フォルダーを開く場合は  _、lppUnk_ を LPMAPIFOLDER 型のポインターにキャストします。</span><span class="sxs-lookup"><span data-stu-id="be5c9-169">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="be5c9-170">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="be5c9-170">MFCMAPI reference</span></span>

<span data-ttu-id="be5c9-171">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be5c9-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="be5c9-172">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="be5c9-172">**File**</span></span>|<span data-ttu-id="be5c9-173">**関数**</span><span class="sxs-lookup"><span data-stu-id="be5c9-173">**Function**</span></span>|<span data-ttu-id="be5c9-174">**コメント**</span><span class="sxs-lookup"><span data-stu-id="be5c9-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="be5c9-175">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="be5c9-175">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="be5c9-176">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="be5c9-176">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="be5c9-177">MFCMAPI は **IMAPISession::OpenEntry メソッド** を使用してオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="be5c9-177">MFCMAPI uses the **IMAPISession::OpenEntry** method to open an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be5c9-178">関連項目</span><span class="sxs-lookup"><span data-stu-id="be5c9-178">See also</span></span>



[<span data-ttu-id="be5c9-179">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="be5c9-179">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="be5c9-180">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="be5c9-180">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md)
  
[<span data-ttu-id="be5c9-181">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="be5c9-181">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)
  
[<span data-ttu-id="be5c9-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="be5c9-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="be5c9-183">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="be5c9-183">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="be5c9-184">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="be5c9-184">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="be5c9-185">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="be5c9-185">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="be5c9-186">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="be5c9-186">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="be5c9-187">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="be5c9-187">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

