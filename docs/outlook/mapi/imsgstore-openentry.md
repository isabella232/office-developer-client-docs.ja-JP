---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409336"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="0f9ff-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0f9ff-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="0f9ff-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f9ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f9ff-105">フォルダーまたはメッセージを開き、さらにアクセスするためのインターフェイスポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="0f9ff-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f9ff-106">Parameters</span></span>

 <span data-ttu-id="0f9ff-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0f9ff-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="0f9ff-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数 _。_</span><span class="sxs-lookup"><span data-stu-id="0f9ff-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="0f9ff-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="0f9ff-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="0f9ff-110">順番開くオブジェクトのエントリ識別子へのポインター。または NULL。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="0f9ff-111">_lな tryid_が NULL に設定されている場合、 **openentry**はメッセージストアのルートフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="0f9ff-112">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="0f9ff-112">_lpInterface_</span></span>
  
> <span data-ttu-id="0f9ff-113">順番開いているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="0f9ff-114">オブジェクトの標準インターフェイス (フォルダーの[imapifolder](imapifolderimapicontainer.md)およびメッセージの[IMessage](imessageimapiprop.md) ) が返されると、NULL 結果が渡されます。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="0f9ff-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0f9ff-115">_ulFlags_</span></span>
  
> <span data-ttu-id="0f9ff-116">順番オブジェクトを開く方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="0f9ff-117">次のフラグを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-117">The following flags can be used:</span></span>
    
<span data-ttu-id="0f9ff-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0f9ff-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="0f9ff-119">ユーザーに対して許可されている最大のネットワークアクセス許可、およびクライアントアプリケーションの最大アクセスを使用して、オブジェクトを開くように要求します。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="0f9ff-120">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、読み取り/書き込みアクセス許可を使用してオブジェクトを開く必要があります。クライアントが読み取り専用アクセス許可を持っている場合は、読み取り専用アクセス許可を使用してオブジェクトを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="0f9ff-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0f9ff-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0f9ff-122">呼び出し元のクライアントがオブジェクトを完全に使用できるようになる前に、 **openentry**が正常に返されることを許可します。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="0f9ff-123">オブジェクトが使用できない場合は、その後のオブジェクト呼び出しでエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="0f9ff-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0f9ff-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="0f9ff-125">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-125">Requests read/write permission.</span></span> <span data-ttu-id="0f9ff-126">既定では、オブジェクトは読み取り専用のアクセス許可で開かれ、読み取り/書き込みアクセス許可が付与されているという前提でクライアントを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="0f9ff-127">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="0f9ff-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="0f9ff-128">読み上げ開かれているオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="0f9ff-129">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="0f9ff-129">_lppUnk_</span></span>
  
> <span data-ttu-id="0f9ff-130">読み上げ開かれているオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0f9ff-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="0f9ff-131">Return value</span></span>

<span data-ttu-id="0f9ff-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f9ff-132">S_OK</span></span> 
  
> <span data-ttu-id="0f9ff-133">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="0f9ff-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0f9ff-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0f9ff-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0f9ff-135">読み取り専用オブジェクトを変更しようとしたか、またはユーザーが十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="0f9ff-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="0f9ff-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="0f9ff-137">ストアをキャッシュモードで開くと、クライアントまたはサービスプロバイダーは**IMsgStore:: openentry**を呼び出し、MAPI_NO_CACHE フラグを設定して、リモートストアのアイテムまたはフォルダーを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="0f9ff-138">リモートサーバーの MDB_ONLINE フラグを使用してメッセージストアを開いた場合、MAPI_NO_CACHE フラグを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f9ff-139">注釈</span><span class="sxs-lookup"><span data-stu-id="0f9ff-139">Remarks</span></span>

<span data-ttu-id="0f9ff-140">**IMsgStore:: openentry**メソッドは、フォルダーまたはメッセージを開き、さらにアクセスするために使用できるインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="0f9ff-141">フォルダーやメッセージなどのパブリックストアでフォルダーエントリを開くときは、 [imapisession:: openentry](imapisession-openentry.md)の代わりに**IMsgStore:: openentry**を使用します。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="0f9ff-142">これにより、プロファイルに複数の Exchange アカウントが定義されている場合に、パブリックフォルダーが正しく機能することが保証されます。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0f9ff-143">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0f9ff-143">Notes to callers</span></span>

<span data-ttu-id="0f9ff-144">_ulflags_パラメーターに MAPI_MODIFY または MAPI_BEST_ACCESS フラグを設定しない限り、フォルダーとメッセージは読み取り専用アクセス許可で自動的に開かれます。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="0f9ff-145">これらのフラグのいずれかを設定しても、特定の種類のアクセス許可は保証されません。付与されるアクセス許可は、メッセージストアプロバイダー、アクセスレベル、およびオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="0f9ff-146">開いているオブジェクトのアクセスレベルを確認するには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="0f9ff-147">**IMsgStore:: openentry**を使用して任意のフォルダーまたはメッセージを開くことができますが、開くフォルダーまたはメッセージの親フォルダーにアクセスできる場合は、通常、 [IMAPIContainer:: openentry](imapicontainer-openentry.md)メソッドを使用する方が高速です。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="0f9ff-148">_lpulobjtype_パラメーターで返された値を調べて、返されたオブジェクトの種類が予想どおりであるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="0f9ff-149">オブジェクトの種類が想定された型ではない場合は、ポインターを_lppunk_パラメーターから適切な型のポインターにキャストします。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="0f9ff-150">たとえば、フォルダーを開いている場合は、 **LPMAPIFOLDER**型のポインターに_lppunk_をキャストします。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0f9ff-151">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="0f9ff-151">MFCMAPI reference</span></span>

<span data-ttu-id="0f9ff-152">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0f9ff-153">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="0f9ff-153">**File**</span></span>|<span data-ttu-id="0f9ff-154">**関数**</span><span class="sxs-lookup"><span data-stu-id="0f9ff-154">**Function**</span></span>|<span data-ttu-id="0f9ff-155">**コメント**</span><span class="sxs-lookup"><span data-stu-id="0f9ff-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0f9ff-156">MAPIFunctions</span><span class="sxs-lookup"><span data-stu-id="0f9ff-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="0f9ff-157">callopenentry</span><span class="sxs-lookup"><span data-stu-id="0f9ff-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="0f9ff-158">mfcmapi は、 **IMsgStore:: openentry**メソッドを使用して、エントリ ID に関連付けられているオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f9ff-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0f9ff-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f9ff-159">See also</span></span>



[<span data-ttu-id="0f9ff-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0f9ff-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="0f9ff-161">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0f9ff-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="0f9ff-162">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0f9ff-162">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

