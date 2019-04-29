---
title: imapisessionopenmsgstore
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
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="d6c2a-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="d6c2a-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="d6c2a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6c2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6c2a-105">メッセージストアを開き、さらにアクセスするための[IMsgStore](imsgstoreimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="d6c2a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d6c2a-106">Parameters</span></span>

<span data-ttu-id="d6c2a-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="d6c2a-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d6c2a-108">順番[共通アドレス] ダイアログボックスとその他の関連する表示の親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="d6c2a-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d6c2a-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="d6c2a-110">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="d6c2a-111">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="d6c2a-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="d6c2a-112">順番開くメッセージストアのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="d6c2a-113">_lな tryid_パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="d6c2a-114">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="d6c2a-114">_lpInterface_</span></span>
  
> <span data-ttu-id="d6c2a-115">順番メッセージストアへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="d6c2a-116">NULL を渡すと、 _lppmdb_パラメーターによって、メッセージストア (**IMsgStore**) の標準インターフェイスへのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="d6c2a-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6c2a-117">_ulFlags_</span></span>
  
> <span data-ttu-id="d6c2a-118">順番オブジェクトを開く方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="d6c2a-119">次のフラグを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="d6c2a-120">MAPI_BEST_ACCESS: ユーザーに対して許可される最大のネットワークアクセス許可、および最大クライアントアプリケーションのアクセス許可を使用して、メッセージストアを開くように要求します。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="d6c2a-121">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、読み取り/書き込みアクセス許可でメッセージストアを開く必要があります。クライアントが読み取り専用アクセス許可を持っている場合は、メッセージストアを読み取り専用アクセス許可で開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="d6c2a-122">MAPI_DEFERRED_ERRORS: **openmsgstore**が正常に復帰することを許可します。これは、メッセージストアが呼び出し元クライアントに完全に使用可能になる前である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="d6c2a-123">メッセージストアが使用できない場合は、後続のオブジェクト呼び出しを行うとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="d6c2a-124">MDB\_NO_DIALOG: ログオンダイアログボックスが表示されないようにします。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="d6c2a-125">このフラグが設定されており、 **openmsgstore**の構成情報が不足しているために、ユーザーのヘルプなしでメッセージストアを開くことができない場合は、MAPI_E_LOGON_FAILED が返されます。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="d6c2a-126">このフラグが設定されていない場合、メッセージストアプロバイダーは、ユーザーに対して名前またはパスワードを修正するか、またはメッセージストアへの接続を確立するために必要なその他のアクションを実行するように求めることができます。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="d6c2a-127">MDB\_NO_MAIL: メールを送信または受信するときに、メッセージストアを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="d6c2a-128">このフラグが設定されている場合、mapi は、このメッセージストアが開かれていることを mapi スプーラーに通知しません。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="d6c2a-129">MDB\_ONLINE: Exchange キャッシュモードでは、クライアントまたはサービスプロバイダーは、MDB_ONLINE を使用してこのメソッドを呼び出して、ローカルメッセージストアへの接続を上書きし、リモートサーバー上でストアを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="d6c2a-130">同じ MAPI セッションで、キャッシュモードおよび非キャッシュモードでは、Exchange ストアを同時に開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="d6c2a-131">キャッシュ済みのメッセージ ストアを既に開いている場合は、このフラグを使用してストアを開く前にストアを閉じるか、このフラグを使用してリモート サーバー上の Exchange ストアを開くことができる新しい MAPI セッションを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="d6c2a-132">MDB_TEMPORARY: MAPI に、メッセージストアが永続的ではなく、メッセージストアテーブルに追加されないようにするように指示します。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="d6c2a-133">このフラグは、メッセージストアにログオンして、プロファイルセクションからプログラムによって情報を取得できるようにするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="d6c2a-134">MDB_WRITE: メッセージストアへの読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="d6c2a-135">_lppmdb_</span><span class="sxs-lookup"><span data-stu-id="d6c2a-135">_lppMDB_</span></span>
  
> <span data-ttu-id="d6c2a-136">読み上げメッセージストアのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6c2a-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="d6c2a-137">Return value</span></span>

<span data-ttu-id="d6c2a-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6c2a-138">S_OK</span></span> 
  
> <span data-ttu-id="d6c2a-139">メッセージストアが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="d6c2a-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d6c2a-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d6c2a-141">ユーザーが十分なアクセス許可を持っていないメッセージストアにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="d6c2a-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d6c2a-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d6c2a-143">_lな tryid_で示されたメッセージストアが存在しません。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="d6c2a-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="d6c2a-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="d6c2a-145">サーバーは、クライアントのコードページをサポートするように構成されていません。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="d6c2a-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="d6c2a-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="d6c2a-147">サーバーは、クライアントのロケール情報をサポートするように構成されていません。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="d6c2a-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="d6c2a-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="d6c2a-149">呼び出しは成功しましたが、メッセージストアプロバイダーにエラー情報があります。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="d6c2a-150">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="d6c2a-151">プロバイダーからエラー情報を取得するには、 [imapisession:: GetLastError](imapisession-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="d6c2a-152">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="d6c2a-153">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6c2a-154">注釈</span><span class="sxs-lookup"><span data-stu-id="d6c2a-154">Remarks</span></span>

<span data-ttu-id="d6c2a-155">**imapisession:: openmsgstore**メソッドは、特定のメッセージストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d6c2a-156">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d6c2a-156">Notes to callers</span></span>

<span data-ttu-id="d6c2a-157">メッセージストアの既定のアクセス許可レベルは、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="d6c2a-158">MDB_WRITE フラグを設定しても、読み取り/書き込みアクセス許可が与えられない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="d6c2a-159">MAPI がメッセージストアに割り当てる最終レベルのアクセス権は、アクセス許可レベル、メッセージストア自体、およびメッセージストアプロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="d6c2a-160">**openmsgstore**を呼び出して、読み取り専用のアクセス許可でメッセージストアを開くと、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="d6c2a-161">ストアの**PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティには、ストア\_MODIFY_OK および store\_CREATE_OK bits が設定されていません。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="d6c2a-162">MAPI_MODIFY フラグが設定された[openentry:: imapisession](imapisession-openentry.md)を使用して、メッセージストアのメッセージまたはフォルダーの1つを開くための呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="d6c2a-163">MAPI_MODIFY フラグが設定された[imapiprop:: openproperty](imapiprop-openproperty.md)を使用して、メッセージストアのメッセージまたはフォルダーのプロパティの1つを開くための呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="d6c2a-164">次のいずれかのメソッドへの呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="d6c2a-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="d6c2a-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="d6c2a-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="d6c2a-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="d6c2a-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="d6c2a-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="d6c2a-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="d6c2a-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="d6c2a-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="d6c2a-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="d6c2a-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="d6c2a-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="d6c2a-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="d6c2a-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="d6c2a-172">コピー先がソースメッセージストアと同じかどうか、または別の読み取り専用ストアであるかどうかにかかわらず、コピーされたメッセージの転送先が読み取り専用である場合、次のメソッドの呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="d6c2a-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="d6c2a-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="d6c2a-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="d6c2a-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="d6c2a-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="d6c2a-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d6c2a-176">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="d6c2a-176">MFCMAPI reference</span></span>

<span data-ttu-id="d6c2a-177">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d6c2a-178">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="d6c2a-178">**File**</span></span>|<span data-ttu-id="d6c2a-179">**関数**</span><span class="sxs-lookup"><span data-stu-id="d6c2a-179">**Function**</span></span>|<span data-ttu-id="d6c2a-180">**コメント**</span><span class="sxs-lookup"><span data-stu-id="d6c2a-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d6c2a-181">MAPIStoreFunctions</span><span class="sxs-lookup"><span data-stu-id="d6c2a-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d6c2a-182">callopenmsgstore</span><span class="sxs-lookup"><span data-stu-id="d6c2a-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="d6c2a-183">mfcmapi は、 **imapisession:: openmsgstore**メソッドを使用して、メッセージストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="d6c2a-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6c2a-184">関連項目</span><span class="sxs-lookup"><span data-stu-id="d6c2a-184">See also</span></span>

- [<span data-ttu-id="d6c2a-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d6c2a-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="d6c2a-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d6c2a-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="d6c2a-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="d6c2a-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="d6c2a-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="d6c2a-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="d6c2a-189">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6c2a-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- <span data-ttu-id="d6c2a-190">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="d6c2a-190">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
- [<span data-ttu-id="d6c2a-191">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="d6c2a-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

