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
# <a name="imsgstoreopenentry"></a><span data-ttu-id="b687c-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b687c-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="b687c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b687c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b687c-105">フォルダーまたはメッセージを開き、さらにアクセスするインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="b687c-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="b687c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b687c-106">Parameters</span></span>

 <span data-ttu-id="b687c-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b687c-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b687c-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト 数  _です。_</span><span class="sxs-lookup"><span data-stu-id="b687c-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="b687c-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b687c-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b687c-110">[in]開くオブジェクトのエントリ識別子 (NULL) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b687c-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="b687c-111">_lpEntryID が_ NULL に設定されている場合 **、OpenEntry は** メッセージ ストアのルート フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="b687c-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="b687c-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b687c-112">_lpInterface_</span></span>
  
> <span data-ttu-id="b687c-113">[in]開いたオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b687c-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="b687c-114">NULL を渡した場合、オブジェクトの標準インターフェイス ([フォルダーの IMAPIFolder](imapifolderimapicontainer.md) とメッセージの [IMessage)](imessageimapiprop.md) が返されます。</span><span class="sxs-lookup"><span data-stu-id="b687c-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="b687c-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b687c-115">_ulFlags_</span></span>
  
> <span data-ttu-id="b687c-116">[in]オブジェクトの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b687c-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="b687c-117">次のフラグを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b687c-117">The following flags can be used:</span></span>
    
<span data-ttu-id="b687c-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b687c-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="b687c-119">ユーザーに許可される最大ネットワークアクセス許可と最大クライアント アプリケーション アクセスを使用してオブジェクトを開く要求。</span><span class="sxs-lookup"><span data-stu-id="b687c-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="b687c-120">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合、オブジェクトは読み取り/書き込みアクセス許可を使用して開く必要があります。クライアントに読み取り専用のアクセス許可がある場合は、オブジェクトを読み取り専用アクセス許可を使用して開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="b687c-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="b687c-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b687c-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="b687c-122">オブジェクトが呼び出し元のクライアントで完全に利用できる前に **、OpenEntry** が正常に返されるのを許可します。</span><span class="sxs-lookup"><span data-stu-id="b687c-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="b687c-123">オブジェクトを使用できない場合は、後続のオブジェクト呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b687c-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="b687c-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b687c-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="b687c-125">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="b687c-125">Requests read/write permission.</span></span> <span data-ttu-id="b687c-126">既定では、オブジェクトは読み取り専用のアクセス許可で開き、クライアントは読み取り/書き込みアクセス許可が付与されるという前提で動作しません。</span><span class="sxs-lookup"><span data-stu-id="b687c-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="b687c-127">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="b687c-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="b687c-128">[out]開いたオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b687c-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="b687c-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="b687c-129">_lppUnk_</span></span>
  
> <span data-ttu-id="b687c-130">[out]開いたオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b687c-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b687c-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="b687c-131">Return value</span></span>

<span data-ttu-id="b687c-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="b687c-132">S_OK</span></span> 
  
> <span data-ttu-id="b687c-133">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b687c-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b687c-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b687c-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b687c-135">読み取り専用オブジェクトを変更しようとしたり、ユーザーのアクセス許可が不十分なオブジェクトにアクセスしようとしたりしました。</span><span class="sxs-lookup"><span data-stu-id="b687c-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="b687c-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="b687c-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="b687c-137">キャッシュ モードでストアを開いた場合、クライアントまたはサービス プロバイダーは **IMsgStore::OpenEntry** を呼び出し、MAPI_NO_CACHE フラグを設定してリモート ストア上のアイテムまたはフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="b687c-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="b687c-138">リモート サーバーで MDB_ONLINE フラグを指定してメッセージ ストアを開く場合は、メッセージ ストア フラグをMAPI_NO_CACHEする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b687c-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b687c-139">注釈</span><span class="sxs-lookup"><span data-stu-id="b687c-139">Remarks</span></span>

<span data-ttu-id="b687c-140">**IMsgStore::OpenEntry** メソッドは、フォルダーまたはメッセージを開き、さらにアクセスするために使用できるインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="b687c-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="b687c-141">フォルダーやメッセージなどのパブリック ストアでフォルダー エントリを開く場合は [、IMAPISession::OpenEntry](imapisession-openentry.md)の代わりに **IMsgStore::OpenEntry** を使用します。</span><span class="sxs-lookup"><span data-stu-id="b687c-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="b687c-142">これにより、複数のアカウントがプロファイルで定義されている場合Exchangeパブリック フォルダーが正しく機能します。</span><span class="sxs-lookup"><span data-stu-id="b687c-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b687c-143">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b687c-143">Notes to callers</span></span>

<span data-ttu-id="b687c-144">_ulFlags_ パラメーターに MAPI_MODIFY または MAPI_BEST_ACCESS フラグを設定しない限り、フォルダーとメッセージは読み取り専用のアクセス許可で自動的に開きます。</span><span class="sxs-lookup"><span data-stu-id="b687c-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="b687c-145">これらのフラグのいずれかを設定しても、特定の種類のアクセス許可は保証されない。付与されるアクセス許可は、メッセージ ストア プロバイダー、アクセス レベル、およびオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="b687c-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="b687c-146">開いたオブジェクトのアクセス レベルを確認するには、そのオブジェクト [(PidTagAccessLevel)](pidtagaccesslevel-canonical-property.md) **PR_ACCESS_LEVELプロパティを** 取得します。</span><span class="sxs-lookup"><span data-stu-id="b687c-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="b687c-147">**IMsgStore::OpenEntry** を使用して任意のフォルダーまたはメッセージを開く場合は、通常 [、IMAPIContainer::OpenEntry](imapicontainer-openentry.md)メソッドを使用する方が、開くフォルダーまたはメッセージの親フォルダーにアクセスできる方が高速です。</span><span class="sxs-lookup"><span data-stu-id="b687c-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="b687c-148">_lpulObjType_ パラメーターで返される値を確認して、返されるオブジェクトの種類が予期した値であるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b687c-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="b687c-149">オブジェクトの種類が予期しない型の場合は  _、lppUnk_ パラメーターから適切な型のポインターにポインターをキャストします。</span><span class="sxs-lookup"><span data-stu-id="b687c-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="b687c-150">たとえば、フォルダーを開く場合は  _、lppUnk_ を **LPMAPIFOLDER** 型のポインターにキャストします。</span><span class="sxs-lookup"><span data-stu-id="b687c-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b687c-151">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="b687c-151">MFCMAPI reference</span></span>

<span data-ttu-id="b687c-152">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b687c-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b687c-153">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="b687c-153">**File**</span></span>|<span data-ttu-id="b687c-154">**関数**</span><span class="sxs-lookup"><span data-stu-id="b687c-154">**Function**</span></span>|<span data-ttu-id="b687c-155">**コメント**</span><span class="sxs-lookup"><span data-stu-id="b687c-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b687c-156">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b687c-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b687c-157">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="b687c-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="b687c-158">MFCMAPI は **、IMsgStore::OpenEntry** メソッドを使用して、エントリ ID に関連付けられたオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="b687c-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b687c-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="b687c-159">See also</span></span>



[<span data-ttu-id="b687c-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b687c-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="b687c-161">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b687c-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="b687c-162">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b687c-162">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

