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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 124208a3f5c6bb300aca3699a04b15e842c46cd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801023"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="ff1af-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ff1af-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="ff1af-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff1af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff1af-105">フォルダーまたはメッセージを開き、さらにアクセスするためのインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="ff1af-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="ff1af-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ff1af-106">Parameters</span></span>

 <span data-ttu-id="ff1af-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ff1af-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ff1af-108">[in]_._ _LpEntryID_パラメーターで指定されたエントリの識別子のバイト数</span><span class="sxs-lookup"><span data-stu-id="ff1af-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="ff1af-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ff1af-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ff1af-110">[in]オブジェクトを開く、または NULL のエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ff1af-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="ff1af-111">_LpEntryID_は、NULL に設定されている場合、 **OpenEntry**は、メッセージ ・ ストアのルート フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="ff1af-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="ff1af-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ff1af-112">_lpInterface_</span></span>
  
> <span data-ttu-id="ff1af-113">[in]開かれているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ff1af-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="ff1af-114">オブジェクトの結果をパラメーターに NULL (このフォルダーには[IMAPIFolder](imapifolderimapicontainer.md) ) とメッセージの[IMessage](imessageimapiprop.md)の標準的なインターフェイスが返されるのです。</span><span class="sxs-lookup"><span data-stu-id="ff1af-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="ff1af-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ff1af-115">_ulFlags_</span></span>
  
> <span data-ttu-id="ff1af-116">[in]オブジェクトを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ff1af-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="ff1af-117">次のフラグを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ff1af-117">The following flags can be used:</span></span>
    
<span data-ttu-id="ff1af-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ff1af-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="ff1af-119">ユーザーおよび最大のクライアント アプリケーションへのアクセスに使用される最大ネットワークのアクセス許可を使用して、オブジェクトを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="ff1af-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="ff1af-120">たとえば、クライアントに読み取り/書き込み権限がある場合、オブジェクト開く必要があります読み取り/書き込みアクセス許可を使用して、クライアントに読み取り専用のアクセス許可がある場合は、読み取り専用のアクセス許可を使用してオブジェクトを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff1af-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="ff1af-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ff1af-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ff1af-122">**OpenEntry**を正常に戻す、可能性のあるオブジェクトが呼び出し元のクライアントに完全に利用できる前にするにを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ff1af-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="ff1af-123">オブジェクトが使用できない場合は、後続のオブジェクトの呼び出しを行うとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ff1af-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="ff1af-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ff1af-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="ff1af-125">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="ff1af-125">Requests read/write permission.</span></span> <span data-ttu-id="ff1af-126">既定では、読み取り専用の権限を持つオブジェクトが開いているし、クライアントが読み取り/書き込み権限が与えられていることを前提に動作しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff1af-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="ff1af-127">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="ff1af-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="ff1af-128">[out]開かれたオブジェクトの型へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ff1af-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="ff1af-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="ff1af-129">_lppUnk_</span></span>
  
> <span data-ttu-id="ff1af-130">[out]開かれたオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ff1af-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ff1af-131">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ff1af-131">Return value</span></span>

<span data-ttu-id="ff1af-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff1af-132">S_OK</span></span> 
  
> <span data-ttu-id="ff1af-133">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="ff1af-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ff1af-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ff1af-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ff1af-135">しようとは、読み取り専用オブジェクトを変更するか、ユーザーが十分なアクセス許可を持っているオブジェクトへのアクセスにしました。</span><span class="sxs-lookup"><span data-stu-id="ff1af-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="ff1af-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="ff1af-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="ff1af-137">ストアをキャッシュ モードで開くときに、クライアントまたはサービス プロバイダーは、 **IMsgStore::OpenEntry**項目、またはリモートのストア上のフォルダーを開くに MAPI_NO_CACHE フラグを設定を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="ff1af-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="ff1af-138">リモート サーバー上で MDB_ONLINE フラグを使用してメッセージ ・ ストアを開く場合、MAPI_NO_CACHE フラグを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ff1af-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff1af-139">注釈</span><span class="sxs-lookup"><span data-stu-id="ff1af-139">Remarks</span></span>

<span data-ttu-id="ff1af-140">**IMsgStore::OpenEntry**メソッドは、フォルダーまたはメッセージを開くし、さらにアクセスするために使用できるインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="ff1af-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ff1af-141">フォルダーやメッセージなどのパブリック ストア上のフォルダーのエントリを開くときは、 [IMAPISession::OpenEntry](imapisession-openentry.md)の代わりに**IMsgStore::OpenEntry**を使用します。</span><span class="sxs-lookup"><span data-stu-id="ff1af-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="ff1af-142">これにより、そのパブリック フォルダー関数正しく複数の Exchange アカウントは、プロファイルで定義されている場合。</span><span class="sxs-lookup"><span data-stu-id="ff1af-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ff1af-143">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ff1af-143">Notes to callers</span></span>

<span data-ttu-id="ff1af-144">フォルダーとメッセージが自動的に開きます読み取り専用のアクセス許可を持つ_ulFlags_パラメーターで、MAPI_MODIFY フラグまたは MAPI_BEST_ACCESS フラグを設定する場合を除き。</span><span class="sxs-lookup"><span data-stu-id="ff1af-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="ff1af-145">これらのフラグのいずれかを設定した場合、アクセス許可の特定の種類は保証されません。付与されたアクセス許可は、メッセージ ストア プロバイダー、ユーザーのアクセス レベル、およびオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="ff1af-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="ff1af-146">開かれたオブジェクトのアクセス レベルを決定するのには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="ff1af-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ff1af-147">任意のフォルダーまたはメッセージを開くには、 **IMsgStore::OpenEntry**を使用できますが、方が通常高速フォルダーまたはメッセージを開くことの親フォルダーにアクセスする場合、 [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ff1af-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="ff1af-148">返されるオブジェクトの種類は、何が必要かどうかを判断するのには_lpulObjType_パラメーターで返される値を確認してください。</span><span class="sxs-lookup"><span data-stu-id="ff1af-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="ff1af-149">オブジェクトの型が予期された型でない場合は、 _lppUnk_パラメーターの適切な型のポインターへのポインターをキャストします。</span><span class="sxs-lookup"><span data-stu-id="ff1af-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="ff1af-150">などのフォルダーを開いている場合は、 **LPMAPIFOLDER**の型のポインターに_lppUnk_をキャストします。</span><span class="sxs-lookup"><span data-stu-id="ff1af-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ff1af-151">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ff1af-151">MFCMAPI reference</span></span>

<span data-ttu-id="ff1af-152">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ff1af-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ff1af-153">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ff1af-153">**File**</span></span>|<span data-ttu-id="ff1af-154">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ff1af-154">**Function**</span></span>|<span data-ttu-id="ff1af-155">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ff1af-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff1af-156">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ff1af-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ff1af-157">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="ff1af-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="ff1af-158">MFCMAPI では、 **IMsgStore::OpenEntry**メソッドを使用して、エントリ ID に関連付けられているオブジェクトを開く</span><span class="sxs-lookup"><span data-stu-id="ff1af-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff1af-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff1af-159">See also</span></span>



[<span data-ttu-id="ff1af-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ff1af-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="ff1af-161">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ff1af-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="ff1af-162">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ff1af-162">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

