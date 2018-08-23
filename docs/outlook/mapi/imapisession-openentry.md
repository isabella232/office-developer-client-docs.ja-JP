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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6234fc737857a7e35f562703802f81ff154b3ee6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591017"
---
# <a name="imapisessionopenentry"></a><span data-ttu-id="51769-103">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="51769-103">IMAPISession::OpenEntry</span></span>

  
  
<span data-ttu-id="51769-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51769-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51769-105">オブジェクトを開き、追加のアクセスのインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="51769-105">Opens an object and returns an interface pointer for additional access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="51769-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="51769-106">Parameters</span></span>

 <span data-ttu-id="51769-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="51769-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="51769-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="51769-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="51769-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="51769-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="51769-110">[in]開くにはオブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="51769-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="51769-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="51769-111">_lpInterface_</span></span>
  
> <span data-ttu-id="51769-112">[in]開かれているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="51769-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="51769-113">NULL を渡すと、オブジェクトの標準的なインターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="51769-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="51769-114">などのオブジェクトを開くことができませんが、メッセージの場合は、標準のインタ フェースは、 [IMessage](imessageimapiprop.md)です。フォルダー、 [IMAPIFolder](imapifolderimapicontainer.md)です。</span><span class="sxs-lookup"><span data-stu-id="51769-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="51769-115">アドレス帳オブジェクトの標準的なインターフェイスは、配布リストおよび[IMailUser](imailuserimapiprop.md)のメッセージング ユーザーの[IDistList](idistlistimapicontainer.md)です。</span><span class="sxs-lookup"><span data-stu-id="51769-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="51769-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="51769-116">_ulFlags_</span></span>
  
> <span data-ttu-id="51769-117">[in]オブジェクトを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="51769-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="51769-118">次のフラグを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="51769-118">The following flags can be used:</span></span>
    
<span data-ttu-id="51769-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="51769-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="51769-120">ユーザーおよび最大のクライアント アプリケーションへのアクセスに使用される最大ネットワークのアクセス許可を使用して、オブジェクトを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="51769-120">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="51769-121">たとえば、クライアントに読み取り/書き込み権限がある場合、オブジェクト開く必要があります読み取り/書き込みアクセス許可を持つクライアントに読み取り専用のアクセス許可がある場合は、読み取り専用権限を持つオブジェクトを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="51769-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span> 
    
<span data-ttu-id="51769-122">MAPI_CACHE_OK</span><span class="sxs-lookup"><span data-stu-id="51769-122">MAPI_CACHE_OK</span></span>
  
> <span data-ttu-id="51769-123">オフライン アドレス帳を含め、すべての手段を使用すると、名前解決を実行できます。</span><span class="sxs-lookup"><span data-stu-id="51769-123">Use all means, including offline address books, to perform name resolution.</span></span>
    
<span data-ttu-id="51769-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="51769-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="51769-125">名前解決を実行するのにには、オフライン アドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="51769-125">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="51769-126">たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。</span><span class="sxs-lookup"><span data-stu-id="51769-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="51769-127">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="51769-127">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="51769-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="51769-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="51769-129">**OpenEntry**を正常に戻す、可能性のあるオブジェクトが呼び出し元のクライアントに完全に利用できる前にするにを使用できます。</span><span class="sxs-lookup"><span data-stu-id="51769-129">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="51769-130">オブジェクトが使用できない場合は、後続のオブジェクトの呼び出しを行うとエラーが発生することができます。</span><span class="sxs-lookup"><span data-stu-id="51769-130">If the object is not available, making a subsequent object call can cause an error.</span></span> 
    
<span data-ttu-id="51769-131">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="51769-131">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="51769-132">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="51769-132">Requests read/write permission.</span></span> <span data-ttu-id="51769-133">既定では、読み取り専用の権限を持つオブジェクトが開いているし、クライアントが読み取り/書き込み権限が与えられていることを前提に動作しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="51769-133">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
<span data-ttu-id="51769-134">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="51769-134">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="51769-135">名前解決を実行するのには、オフライン アドレス帳を使用しません。</span><span class="sxs-lookup"><span data-stu-id="51769-135">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="51769-136">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="51769-136">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="51769-137">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="51769-137">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="51769-138">ソフトとしてマークされているアイテムの削除を表示する (つまりにいる削除済みアイテムの保存時間フェーズ)。</span><span class="sxs-lookup"><span data-stu-id="51769-138">Show items that are currently marked as soft deleted (that is, they are in the deleted item retention time phase).</span></span>
    
 <span data-ttu-id="51769-139">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="51769-139">_lpulObjType_</span></span>
  
> <span data-ttu-id="51769-140">[out]開かれたオブジェクトの型へのポインター。</span><span class="sxs-lookup"><span data-stu-id="51769-140">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="51769-141">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="51769-141">_lppUnk_</span></span>
  
> <span data-ttu-id="51769-142">[out]開かれたオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="51769-142">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51769-143">�߂�l</span><span class="sxs-lookup"><span data-stu-id="51769-143">Return value</span></span>

<span data-ttu-id="51769-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="51769-144">S_OK</span></span> 
  
> <span data-ttu-id="51769-145">オブジェクトが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="51769-145">The object was opened successfully.</span></span>
    
<span data-ttu-id="51769-146">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="51769-146">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="51769-147">読み取り専用オブジェクトを変更しようとしましたまたは、ユーザーが十分なアクセス許可を持っているオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="51769-147">An attempt was made to modify a read-only object or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="51769-148">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="51769-148">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="51769-149">_LpEntryID_パラメーターで渡されたエントリの識別子に関連付けられているオブジェクトではありません。</span><span class="sxs-lookup"><span data-stu-id="51769-149">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="51769-150">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="51769-150">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="51769-151">_LpEntryID_パラメーターで渡されたエントリ id が、認識できない形式です。</span><span class="sxs-lookup"><span data-stu-id="51769-151">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="51769-152">この値は通常、オブジェクトが含まれているサービス プロバイダーが開いていない場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="51769-152">This value is typically returned if the service provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="51769-153">注釈</span><span class="sxs-lookup"><span data-stu-id="51769-153">Remarks</span></span>

<span data-ttu-id="51769-154">メッセージが保存、またはアドレス帳オブジェクト、インターフェイスへのポインターを返す**IMAPISession::OpenEntry**メソッドが表示は、オブジェクトへのアクセスに使用できます。</span><span class="sxs-lookup"><span data-stu-id="51769-154">The **IMAPISession::OpenEntry** method opens a message store or address book object, returning a pointer to an interface that can be used to access the object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="51769-155">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="51769-155">Notes to callers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51769-156">フォルダーやメッセージなどのパブリック ストア上のフォルダーのエントリを開くときは、 **IMAPISession::OpenEntry**の代わりに[IMsgStore::OpenEntry](imsgstore-openentry.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="51769-156">When opening folder entries on a public store, such as folders and messages, use [IMsgStore::OpenEntry](imsgstore-openentry.md) instead of **IMAPISession::OpenEntry**.</span></span> <span data-ttu-id="51769-157">これにより、そのパブリック フォルダー関数正しく複数の Exchange アカウントは、プロファイルで定義されている場合。</span><span class="sxs-lookup"><span data-stu-id="51769-157">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
<span data-ttu-id="51769-158">開こうとしているオブジェクトの種類がわからない場合にのみ、 **IMAPISession::OpenEntry**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="51769-158">Call **IMAPISession::OpenEntry** only when you do not know what kind of object that you are opening.</span></span> <span data-ttu-id="51769-159">フォルダーまたはメッセージを開いていることがわかっている場合は、 [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="51769-159">If you know that you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="51769-160">アドレス帳コンテナーである、メッセージング ユーザー、または配布リストが置かれていることがわかっている場合は、[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="51769-160">If you know that you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="51769-161">これらの具体的な方法は、 **IMAPISession::OpenEntry**よりも高速です。</span><span class="sxs-lookup"><span data-stu-id="51769-161">These more specific methods are faster than **IMAPISession::OpenEntry**.</span></span> 
  
<span data-ttu-id="51769-162">MAPI は、 _ulFlags_パラメーターで、MAPI_MODIFY フラグまたは MAPI_BEST_ACCESS フラグを設定する場合を除き、読み取り専用のアクセス許可を持つすべてのオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="51769-162">MAPI opens all objects with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="51769-163">これらのフラグのいずれかを設定では特定の種類のアクセスは保証されません。与えられたアクセス許可は、サービス プロバイダー、アクセス レベル、およびオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="51769-163">Setting one of these flags does not guarantee a particular type of access; the permissions that are granted depend on the service provider, the access level, and the object.</span></span> <span data-ttu-id="51769-164">開かれたオブジェクトのアクセス レベルを決定するのには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="51769-164">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="51769-165">メッセージ ストアのエントリ id を指すように**IMAPISession::OpenEntry**と_lpEntryID_の設定を呼び出すことは MDB_NO_DIALOG フラグを指定して[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドを呼び出す場合と同じ設定します。</span><span class="sxs-lookup"><span data-stu-id="51769-165">Calling **IMAPISession::OpenEntry** and setting  _lpEntryID_ to point to the entry identifier of a message store is the same as calling the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method with the MDB_NO_DIALOG flag set.</span></span> <span data-ttu-id="51769-166">フラグの設定も同等ですが、 **OpenMsgStore**と読み取り/書き込みアクセス許可を要求することを除いては、MAPI_MODIFY の代わりに MDB_WRITE フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="51769-166">The flag settings are also equivalent, except that to request read/write permission with **OpenMsgStore**, you must set the MDB_WRITE flag instead of MAPI_MODIFY.</span></span> 
  
<span data-ttu-id="51769-167">返されるオブジェクトの型は、何が必要かどうかを判断するのには_lpulObjType_パラメーターで返される値を確認してください。</span><span class="sxs-lookup"><span data-stu-id="51769-167">Check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what you expected.</span></span> <span data-ttu-id="51769-168">オブジェクトの型が予測した型でない場合は、 _lppUnk_パラメーターの適切な型のポインターへのポインターをキャストします。</span><span class="sxs-lookup"><span data-stu-id="51769-168">If the object type is not the type that you expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="51769-169">などのフォルダーを開いている場合は、LPMAPIFOLDER の型のポインターに_lppUnk_をキャストします。</span><span class="sxs-lookup"><span data-stu-id="51769-169">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="51769-170">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="51769-170">MFCMAPI reference</span></span>

<span data-ttu-id="51769-171">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="51769-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="51769-172">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="51769-172">**File**</span></span>|<span data-ttu-id="51769-173">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="51769-173">**Function**</span></span>|<span data-ttu-id="51769-174">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="51769-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="51769-175">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="51769-175">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="51769-176">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="51769-176">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="51769-177">MFCMAPI では、 **IMAPISession::OpenEntry**メソッドを使用して、オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="51769-177">MFCMAPI uses the **IMAPISession::OpenEntry** method to open an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51769-178">関連項目</span><span class="sxs-lookup"><span data-stu-id="51769-178">See also</span></span>



[<span data-ttu-id="51769-179">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="51769-179">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="51769-180">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="51769-180">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md)
  
[<span data-ttu-id="51769-181">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="51769-181">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)
  
[<span data-ttu-id="51769-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="51769-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="51769-183">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="51769-183">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="51769-184">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="51769-184">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="51769-185">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="51769-185">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="51769-186">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="51769-186">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="51769-187">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="51769-187">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

