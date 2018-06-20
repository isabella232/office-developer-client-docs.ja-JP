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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 983c22772acfea7837e85d409b7928a35aed91ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800699"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="1b311-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="1b311-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="1b311-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b311-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b311-105">メッセージ ストアを開き、さらにアクセスするための[IMsgStore](imsgstoreimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="1b311-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="1b311-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1b311-106">Parameters</span></span>

<span data-ttu-id="1b311-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1b311-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="1b311-108">[in]表示に関連して、共通のアドレス] ダイアログ ボックスおよびその他の親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="1b311-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="1b311-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1b311-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="1b311-110">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="1b311-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="1b311-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1b311-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="1b311-112">[in]メッセージ ・ ストアを開くことのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1b311-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="1b311-113">_LpEntryID_パラメーターを NULL にする必要がありますはできません。</span><span class="sxs-lookup"><span data-stu-id="1b311-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="1b311-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1b311-114">_lpInterface_</span></span>
  
> <span data-ttu-id="1b311-115">[in]メッセージ ストアへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1b311-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="1b311-116">メッセージ ストア (**IMsgStore**) の標準的なインターフェイスへのポインターを返すに_lppMDB_パラメーターは、NULL を渡すことです。</span><span class="sxs-lookup"><span data-stu-id="1b311-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="1b311-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b311-117">_ulFlags_</span></span>
  
> <span data-ttu-id="1b311-118">[in]オブジェクトを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="1b311-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="1b311-119">次のフラグを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="1b311-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="1b311-120">MAPI_BEST_ACCESS: 要求の最大のネットワーク アクセス許可を持つメッセージ ・ ストアを開くことは許可ユーザーと、最大のクライアントのアプリケーションのアクセス許可。</span><span class="sxs-lookup"><span data-stu-id="1b311-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="1b311-121">たとえば、クライアントに読み取り/書き込み権限がある場合は、メッセージ ・ ストア開く必要があります読み取り/書き込みアクセス許可を持つクライアントに読み取り専用のアクセス許可がある場合は、読み取り専用のアクセス許可を持つメッセージ ・ ストアを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b311-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="1b311-122">MAPI_DEFERRED_ERRORS: 正常に完了する**OpenMsgStore**を使用する可能性のあるメッセージの前にストアは、呼び出し側のクライアントに完全に使用可能。</span><span class="sxs-lookup"><span data-stu-id="1b311-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="1b311-123">メッセージ ・ ストアを使用できない場合は、後続のオブジェクトの呼び出しを行うとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1b311-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="1b311-124">MDB\_NO_DIALOG: ログオン] ダイアログ ボックスが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="1b311-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="1b311-125">このフラグが設定し、 **OpenMsgStore**が不足している構成については、ユーザーのヘルプを表示しないメッセージ ストアを開くには、MAPI_E_LOGON_FAILED が返されます。</span><span class="sxs-lookup"><span data-stu-id="1b311-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="1b311-126">このフラグが設定されていない場合、メッセージ ストア プロバイダーはユーザー名またはパスワードを修正するか、メッセージ ・ ストアへの接続を確立するために必要なその他のアクションを実行するを求めることができます。</span><span class="sxs-lookup"><span data-stu-id="1b311-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="1b311-127">MDB\_NO_MAIL: メールの送受信のメッセージ ・ ストアを使用いない必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b311-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="1b311-128">このフラグを設定すると、MAPI 通知されません、MAPI スプーラーを無効このメッセージ ・ ストアが開かれることです。</span><span class="sxs-lookup"><span data-stu-id="1b311-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="1b311-129">MDB\_オンライン: で Exchange キャッシュ モード、クライアントまたはサービス プロバイダーは、ローカル メッセージ ストアへの接続をオーバーライドし、リモート サーバー上のストアを開くには MDB_ONLINE でこのメソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="1b311-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="1b311-130">同じ MAPI セッションで同時にキャッシュ モードと非キャッシュ モードで、Exchange ストアを開くことができません。</span><span class="sxs-lookup"><span data-stu-id="1b311-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="1b311-131">キャッシュされたメッセージ ストアを既に開いている場合、このフラグで開き、またはこのフラグを使用してリモート サーバー上の Exchange ストアを開く新しい MAPI セッションを開始する前にストアを閉じる必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="1b311-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="1b311-132">MDB_TEMPORARY: は、メッセージ ・ ストアは永続的ではありませんし、メッセージ ストアのテーブルに追加できませんする必要があります、MAPI を指示します。</span><span class="sxs-lookup"><span data-stu-id="1b311-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="1b311-133">このフラグを使用して、プロファイル セクションから情報をプログラムによって取得できるように、メッセージ ストアにログオンします。</span><span class="sxs-lookup"><span data-stu-id="1b311-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="1b311-134">MDB_WRITE: 要求読み取り/書き込み、メッセージ ・ ストアにアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="1b311-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="1b311-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="1b311-135">_lppMDB_</span></span>
  
> <span data-ttu-id="1b311-136">[out]メッセージ ・ ストアのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1b311-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b311-137">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1b311-137">Return value</span></span>

<span data-ttu-id="1b311-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b311-138">S_OK</span></span> 
  
> <span data-ttu-id="1b311-139">メッセージ ・ ストアが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="1b311-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="1b311-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1b311-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="1b311-141">ユーザーが十分なアクセス許可を持っているメッセージ ストアにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="1b311-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="1b311-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1b311-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1b311-143">_LpEntryID_で指定されたメッセージ ・ ストアが存在しません。</span><span class="sxs-lookup"><span data-stu-id="1b311-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="1b311-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="1b311-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="1b311-145">サーバーは、クライアントのコード ページをサポートするために構成されていません。</span><span class="sxs-lookup"><span data-stu-id="1b311-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="1b311-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="1b311-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="1b311-147">サーバーは、クライアントのロケール情報をサポートするために構成されていません。</span><span class="sxs-lookup"><span data-stu-id="1b311-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="1b311-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="1b311-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="1b311-149">呼び出しが成功したが、メッセージ ストア プロバイダーが使用可能なエラー情報を持ちます。</span><span class="sxs-lookup"><span data-stu-id="1b311-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="1b311-150">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b311-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="1b311-151">プロバイダーからエラー情報を取得するには、 [IMAPISession::GetLastError](imapisession-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1b311-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="1b311-152">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="1b311-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="1b311-153">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b311-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b311-154">備考</span><span class="sxs-lookup"><span data-stu-id="1b311-154">Remarks</span></span>

<span data-ttu-id="1b311-155">**IMAPISession::OpenMsgStore**メソッドは、特定のメッセージ ストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="1b311-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1b311-156">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1b311-156">Notes to callers</span></span>

<span data-ttu-id="1b311-157">メッセージ ストアの既定のアクセス許可レベルは、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="1b311-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="1b311-158">MDB_WRITE フラグを設定した場合、まだ可能性がありますは許可されません読み取り/書き込みアクセス許可。</span><span class="sxs-lookup"><span data-stu-id="1b311-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="1b311-159">MAPI の割り当て、メッセージ ・ ストアには、アクセス許可レベルに依存しているアクセスの最後のレベル、メッセージ ・ ストア自体、およびメッセージ ストア プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="1b311-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="1b311-160">読み取り専用アクセス権を持つメッセージ ・ ストアを開くには、 **OpenMsgStore**を呼び出すと、次が発生します。</span><span class="sxs-lookup"><span data-stu-id="1b311-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="1b311-161">店舗の**PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティには、そのストアがない\_MODIFY_OK とストア\_CREATE_OK ビットをセットします。</span><span class="sxs-lookup"><span data-stu-id="1b311-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="1b311-162">MAPI_MODIFY フラグを設定して[IMAPISession::OpenEntry](imapisession-openentry.md)を使用してメッセージ ストアのメッセージまたはフォルダーのいずれかを開く呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="1b311-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="1b311-163">MAPI_MODIFY フラグを使用して[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を使用してメッセージ ストアのメッセージまたはフォルダーのプロパティのいずれかを開く呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="1b311-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="1b311-164">次の方法のいずれかの呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="1b311-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="1b311-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="1b311-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="1b311-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="1b311-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="1b311-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="1b311-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="1b311-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="1b311-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="1b311-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="1b311-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="1b311-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="1b311-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="1b311-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="1b311-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="1b311-172">コピーしたメッセージの送信先は、読み取り専用でリンク先が元のメッセージ ストアの場合と同じまたは別の読み取り専用ストアは、かどうかの場合、次のメソッドへの呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="1b311-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="1b311-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="1b311-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="1b311-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="1b311-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="1b311-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="1b311-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1b311-176">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="1b311-176">MFCMAPI reference</span></span>

<span data-ttu-id="1b311-177">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="1b311-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1b311-178">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="1b311-178">**File**</span></span>|<span data-ttu-id="1b311-179">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="1b311-179">**Function**</span></span>|<span data-ttu-id="1b311-180">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="1b311-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1b311-181">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1b311-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1b311-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="1b311-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="1b311-183">MFCMAPI では、 **IMAPISession::OpenMsgStore**メソッドを使用して、メッセージ ストアを開けません。</span><span class="sxs-lookup"><span data-stu-id="1b311-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b311-184">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b311-184">See also</span></span>

- [<span data-ttu-id="1b311-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1b311-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="1b311-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1b311-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="1b311-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1b311-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="1b311-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="1b311-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="1b311-189">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b311-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- <span data-ttu-id="1b311-190">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1b311-190">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
- [<span data-ttu-id="1b311-191">エラー処理のためのマクロを使用してください。</span><span class="sxs-lookup"><span data-stu-id="1b311-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

