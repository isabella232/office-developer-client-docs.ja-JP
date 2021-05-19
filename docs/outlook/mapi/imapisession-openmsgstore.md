---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418023"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="21802-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="21802-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="21802-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21802-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21802-105">メッセージ ストアを開き、さらにアクセスする [IMsgStore ポインター](imsgstoreimapiprop.md) を返します。</span><span class="sxs-lookup"><span data-stu-id="21802-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a><span data-ttu-id="21802-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="21802-106">Parameters</span></span>

<span data-ttu-id="21802-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="21802-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="21802-108">[in]共通のアドレス ダイアログ ボックスの親ウィンドウへのハンドルと、その他の関連する表示。</span><span class="sxs-lookup"><span data-stu-id="21802-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="21802-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="21802-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="21802-110">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="21802-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="21802-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="21802-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="21802-112">[in]開くメッセージ ストアのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="21802-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="21802-113">_lpEntryID パラメーター_ は NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="21802-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="21802-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="21802-114">_lpInterface_</span></span>
  
> <span data-ttu-id="21802-115">[in]メッセージ ストアへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="21802-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="21802-116">NULL を渡す場合  _、lppMDB_ パラメーターはメッセージ ストア **(IMsgStore)** の標準インターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="21802-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="21802-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="21802-117">_ulFlags_</span></span>
  
> <span data-ttu-id="21802-118">[in]オブジェクトの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="21802-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="21802-119">次のフラグを使用できます。</span><span class="sxs-lookup"><span data-stu-id="21802-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="21802-120">MAPI_BEST_ACCESS: ユーザーに許可される最大ネットワークアクセス許可とクライアント アプリケーションの最大アクセス許可を使用してメッセージ ストアを開く要求。</span><span class="sxs-lookup"><span data-stu-id="21802-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="21802-121">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、メッセージ ストアを読み取り/書き込みアクセス許可で開く必要があります。クライアントに読み取り専用のアクセス許可がある場合は、メッセージ ストアを読み取り専用のアクセス許可で開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="21802-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="21802-122">MAPI_DEFERRED_ERRORS: メッセージ ストアが呼び出し元のクライアントで完全に利用できる前に **、OpenMsgStore** が正常に返されるのを許可します。</span><span class="sxs-lookup"><span data-stu-id="21802-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="21802-123">メッセージ ストアを使用できない場合は、後続のオブジェクト呼び出しを実行するとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="21802-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="21802-124">MDB \_ NO_DIALOG: ログオン ダイアログ ボックスの表示を防止します。</span><span class="sxs-lookup"><span data-stu-id="21802-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="21802-125">このフラグが設定されている場合 **、OpenMsgStore** には、ユーザーの助けを借りずにメッセージ ストアを開くのに十分な構成情報がない場合は、メッセージ ストアMAPI_E_LOGON_FAILED。</span><span class="sxs-lookup"><span data-stu-id="21802-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="21802-126">このフラグが設定されていない場合、メッセージ ストア プロバイダーは、名前またはパスワードを修正するか、メッセージ ストアへの接続を確立するために必要なその他のアクションを実行するようにユーザーに求められます。</span><span class="sxs-lookup"><span data-stu-id="21802-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="21802-127">MDB NO_MAIL: メッセージ ストアは、 \_ メールの送受信には使用できません。</span><span class="sxs-lookup"><span data-stu-id="21802-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="21802-128">このフラグが設定されている場合、MAPI は、このメッセージ ストアが開いているという MAPI スプーラーに通知されません。</span><span class="sxs-lookup"><span data-stu-id="21802-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="21802-129">MDB ONLINE: キャッシュ Exchange モードでは、クライアントまたはサービス プロバイダーは MDB_ONLINE でこのメソッドを呼び出して、ローカル メッセージ ストアへの接続をオーバーライドし、リモート サーバー上でストアを開きます。 \_</span><span class="sxs-lookup"><span data-stu-id="21802-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="21802-130">同じ MAPI セッションExchangeキャッシュ モードと非キャッシュ モードで、キャッシュ ストアを開くことができません。</span><span class="sxs-lookup"><span data-stu-id="21802-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="21802-131">キャッシュ済みのメッセージ ストアを既に開いている場合は、このフラグを使用してストアを開く前にストアを閉じるか、このフラグを使用してリモート サーバー上の Exchange ストアを開くことができる新しい MAPI セッションを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="21802-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="21802-132">MDB_TEMPORARY: メッセージ ストアが永続的ではなく、メッセージ ストア テーブルに追加しないよう MAPI に指示します。</span><span class="sxs-lookup"><span data-stu-id="21802-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="21802-133">このフラグは、メッセージ ストアにログオンするために使用され、プロファイル セクションからプログラムによって情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="21802-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="21802-134">MDB_WRITE: メッセージ ストアへの読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="21802-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="21802-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="21802-135">_lppMDB_</span></span>
  
> <span data-ttu-id="21802-136">[out]メッセージ ストアのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="21802-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="21802-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="21802-137">Return value</span></span>

<span data-ttu-id="21802-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="21802-138">S_OK</span></span> 
  
> <span data-ttu-id="21802-139">メッセージ ストアが正常に開かされました。</span><span class="sxs-lookup"><span data-stu-id="21802-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="21802-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="21802-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="21802-141">ユーザーのアクセス許可が不十分なメッセージ ストアにアクセスしようとした。</span><span class="sxs-lookup"><span data-stu-id="21802-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="21802-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="21802-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="21802-143">_lpEntryID_ で示されるメッセージ ストアが存在しません。</span><span class="sxs-lookup"><span data-stu-id="21802-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="21802-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="21802-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="21802-145">サーバーは、クライアントのコード ページをサポートするように構成されていません。</span><span class="sxs-lookup"><span data-stu-id="21802-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="21802-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="21802-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="21802-147">サーバーは、クライアントのロケール情報をサポートするように構成されていません。</span><span class="sxs-lookup"><span data-stu-id="21802-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="21802-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="21802-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="21802-149">呼び出しは成功しましたが、メッセージ ストア プロバイダーにエラー情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="21802-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="21802-150">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="21802-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="21802-151">プロバイダーからエラー情報を取得するには [、IMAPISession::GetLastError メソッドを呼び出](imapisession-getlasterror.md) します。</span><span class="sxs-lookup"><span data-stu-id="21802-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="21802-152">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="21802-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="21802-153">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="21802-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21802-154">注釈</span><span class="sxs-lookup"><span data-stu-id="21802-154">Remarks</span></span>

<span data-ttu-id="21802-155">**IMAPISession::OpenMsgStore** メソッドは、特定のメッセージ ストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="21802-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="21802-156">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="21802-156">Notes to callers</span></span>

<span data-ttu-id="21802-157">メッセージ ストアの既定のアクセス許可レベルは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="21802-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="21802-158">このフラグを設定MDB_WRITE、引き続き読み取り/書き込みアクセス許可が付与されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="21802-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="21802-159">MAPI がメッセージ ストアに割り当てるアクセスの最終レベルは、アクセス許可レベル、メッセージ ストア自体、およびメッセージ ストア プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="21802-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="21802-160">**OpenMsgStore を呼び出して** 読み取り専用のアクセス許可を持つメッセージ ストアを開く場合、次の処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="21802-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="21802-161">ストアの **PR \_** STORE_SUPPORT_MASK ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティには、STORE の値と STORE MODIFY_OKが設定 \_ \_ CREATE_OKされません。</span><span class="sxs-lookup"><span data-stu-id="21802-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="21802-162">[IMAPISession::OpenEntry](imapisession-openentry.md)を使用してメッセージ ストアのメッセージまたはフォルダーの 1 つを開く呼び出しは、MAPI_MODIFYが失敗します。</span><span class="sxs-lookup"><span data-stu-id="21802-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="21802-163">[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を使用してメッセージ ストアのメッセージまたはフォルダーのプロパティの 1 つを開く呼び出しは、MAPI_MODIFY失敗します。</span><span class="sxs-lookup"><span data-stu-id="21802-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="21802-164">次のメソッドの呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="21802-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="21802-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="21802-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="21802-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="21802-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="21802-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="21802-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="21802-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="21802-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="21802-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="21802-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="21802-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="21802-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="21802-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="21802-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="21802-172">コピー先がソース メッセージ ストアと同じか、別の読み取り専用ストアである場合でも、コピーされたメッセージの送信先が読み取り専用の場合、次のメソッドの呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="21802-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="21802-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="21802-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="21802-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="21802-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="21802-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="21802-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="21802-176">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="21802-176">MFCMAPI reference</span></span>

<span data-ttu-id="21802-177">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21802-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="21802-178">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="21802-178">**File**</span></span>|<span data-ttu-id="21802-179">**関数**</span><span class="sxs-lookup"><span data-stu-id="21802-179">**Function**</span></span>|<span data-ttu-id="21802-180">**コメント**</span><span class="sxs-lookup"><span data-stu-id="21802-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21802-181">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="21802-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="21802-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="21802-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="21802-183">MFCMAPI は **IMAPISession::OpenMsgStore** メソッドを使用してメッセージ ストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="21802-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21802-184">関連項目</span><span class="sxs-lookup"><span data-stu-id="21802-184">See also</span></span>

- [<span data-ttu-id="21802-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="21802-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="21802-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="21802-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="21802-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="21802-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="21802-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="21802-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="21802-189">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="21802-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- <span data-ttu-id="21802-190">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="21802-190">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
- [<span data-ttu-id="21802-191">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="21802-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

