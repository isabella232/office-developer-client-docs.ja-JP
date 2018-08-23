---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 619357a608dd160cbe4811cc7db7ae3b392db858
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576891"
---
# <a name="imslogonopenentry"></a><span data-ttu-id="566fb-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="566fb-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="566fb-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="566fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="566fb-105">フォルダーまたはメッセージのオブジェクトを開くし、さらにアクセスを提供するオブジェクトへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="566fb-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulOpenFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="566fb-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="566fb-106">Parameters</span></span>

 <span data-ttu-id="566fb-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="566fb-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="566fb-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="566fb-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="566fb-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="566fb-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="566fb-110">[in]フォルダーまたはメッセージを開くにはオブジェクトのエントリ id のアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="566fb-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="566fb-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="566fb-111">_lpInterface_</span></span>
  
> <span data-ttu-id="566fb-112">[in]オブジェクトのインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="566fb-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="566fb-113">NULL を渡すには、このようなオブジェクトの標準的なインタ フェースにオブジェクトをキャストすることを示します。</span><span class="sxs-lookup"><span data-stu-id="566fb-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="566fb-114">_LpInterface_パラメーターは、オブジェクトの適切なインターフェイスの識別子を設定することも。</span><span class="sxs-lookup"><span data-stu-id="566fb-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="566fb-115">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="566fb-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="566fb-116">[in]オブジェクトを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="566fb-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="566fb-117">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="566fb-117">The following flags can be set:</span></span>
    
<span data-ttu-id="566fb-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="566fb-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="566fb-119">ユーザーと最大のクライアント アプリケーションのアクセス許可で許可される最大のアクセス許可を持つオブジェクトを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="566fb-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="566fb-120">たとえば、クライアントに読み取り/書き込み権限がある場合は、オブジェクトを開くと読み取り/書き込みアクセス許可を持つクライアントに読み取り専用のアクセス許可がある場合は、読み取り専用権限を持つオブジェクトが開かれます。</span><span class="sxs-lookup"><span data-stu-id="566fb-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="566fb-121">クライアントは、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) のプロパティを取得することによって、アクセス許可レベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="566fb-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="566fb-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="566fb-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="566fb-123">呼び出しは、基になるオブジェクトが呼び出し元のアプリケーションに利用可能でない場合でも、成功するために許可されています。</span><span class="sxs-lookup"><span data-stu-id="566fb-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="566fb-124">オブジェクトが使用できない場合は、オブジェクトへの後続の呼び出しはエラーを返すことがあります。</span><span class="sxs-lookup"><span data-stu-id="566fb-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="566fb-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="566fb-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="566fb-126">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="566fb-126">Requests read/write permission.</span></span> <span data-ttu-id="566fb-127">既定では、読み取り専用の権限を持つオブジェクトが作成され、クライアントが読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="566fb-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="566fb-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="566fb-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="566fb-129">[out]開かれたオブジェクトの型へのポインター。</span><span class="sxs-lookup"><span data-stu-id="566fb-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="566fb-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="566fb-130">_lppUnk_</span></span>
  
> <span data-ttu-id="566fb-131">[out]開かれたオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="566fb-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="566fb-132">�߂�l</span><span class="sxs-lookup"><span data-stu-id="566fb-132">Return value</span></span>

<span data-ttu-id="566fb-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="566fb-133">S_OK</span></span> 
  
> <span data-ttu-id="566fb-134">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="566fb-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="566fb-135">����</span><span class="sxs-lookup"><span data-stu-id="566fb-135">Remarks</span></span>

<span data-ttu-id="566fb-136">MAPI は、メッセージ ストア内のフォルダーまたはメッセージを開くに**IMSLogon::OpenEntry**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="566fb-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="566fb-137">MAPI を開くにはオブジェクトのエントリ id を渡します。</span><span class="sxs-lookup"><span data-stu-id="566fb-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="566fb-138">メッセージ ストア プロバイダーは、 _lppUnk_パラメーターで指定したオブジェクトにさらにアクセスできるようにするためのポインターを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="566fb-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="566fb-139">MAPI では、 **IMSLogon::OpenEntry**を呼び出し、前に、最初に指定したメッセージまたはフォルダーのエントリ id と一致しているこのメッセージ ストア プロバイダーが登録されているいずれかを決定します。</span><span class="sxs-lookup"><span data-stu-id="566fb-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="566fb-140">エントリの識別子では、ストア プロバイダーを登録する方法の詳細については[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="566fb-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="566fb-141">**IMSLogon::OpenEntry**は、メッセージ ストアのオブジェクトの[IMsgStore::OpenEntry](imsgstore-openentry.md)メソッドをクライアントに**IMSLogon::OpenEntry**は呼び出しませんMAPI は、 **IMAPISession::OpenEntry**メソッドを処理するときに**IMSLogon::OpenEntry**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="566fb-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="566fb-142">オブジェクトの**IMSLogon::OpenEntry**を使用して開く必要がありますメッセージを使用して開かれたオブジェクトの格納オブジェクトとまったく同じに扱われます具体的には、この呼び出しを使用して開かれたオブジェクトは、メッセージ ストア オブジェクトを離したとき無効にするべき。</span><span class="sxs-lookup"><span data-stu-id="566fb-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="566fb-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="566fb-143">See also</span></span>



[<span data-ttu-id="566fb-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="566fb-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="566fb-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="566fb-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="566fb-146">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="566fb-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

