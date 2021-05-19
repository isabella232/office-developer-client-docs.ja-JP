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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416301"
---
# <a name="imslogonopenentry"></a><span data-ttu-id="98693-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="98693-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="98693-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98693-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98693-105">フォルダーまたはメッセージ オブジェクトを開き、オブジェクトへのポインターを返して、さらにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="98693-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="98693-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="98693-106">Parameters</span></span>

 <span data-ttu-id="98693-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="98693-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="98693-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="98693-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="98693-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="98693-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="98693-110">[in]開くフォルダーまたはメッセージ オブジェクトのエントリ識別子のアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="98693-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="98693-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="98693-111">_lpInterface_</span></span>
  
> <span data-ttu-id="98693-112">[in]オブジェクトのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="98693-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="98693-113">NULL を渡す場合は、オブジェクトがそのようなオブジェクトの標準インターフェイスにキャストされます。</span><span class="sxs-lookup"><span data-stu-id="98693-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="98693-114">_lpInterface パラメーター_ は、オブジェクトの適切なインターフェイスの識別子に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="98693-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="98693-115">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="98693-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="98693-116">[in]オブジェクトの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="98693-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="98693-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="98693-117">The following flags can be set:</span></span>
    
<span data-ttu-id="98693-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="98693-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="98693-119">オブジェクトは、ユーザーに許可される最大アクセス許可とクライアント アプリケーションの最大アクセス許可で開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="98693-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="98693-120">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合、オブジェクトは読み取り/書き込みアクセス許可で開きます。クライアントに読み取り専用のアクセス許可がある場合、オブジェクトは読み取り専用のアクセス許可で開きます。</span><span class="sxs-lookup"><span data-stu-id="98693-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="98693-121">クライアントは、アクセス許可レベルを取得するには、PR_ACCESS_LEVEL **(** [PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="98693-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="98693-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="98693-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="98693-123">呼び出し元のオブジェクトが呼び出し元のアプリケーションで使用できない場合でも、呼び出しは成功できます。</span><span class="sxs-lookup"><span data-stu-id="98693-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="98693-124">オブジェクトが使用できない場合は、そのオブジェクトに対する後続の呼び出しでエラーが返される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="98693-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="98693-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="98693-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="98693-126">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="98693-126">Requests read/write permission.</span></span> <span data-ttu-id="98693-127">既定では、オブジェクトは読み取り専用のアクセス許可で作成され、クライアントは読み取り/書き込みアクセス許可が付与されているという前提で動作しません。</span><span class="sxs-lookup"><span data-stu-id="98693-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="98693-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="98693-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="98693-129">[out]開いたオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="98693-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="98693-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="98693-130">_lppUnk_</span></span>
  
> <span data-ttu-id="98693-131">[out]開いたオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="98693-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98693-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="98693-132">Return value</span></span>

<span data-ttu-id="98693-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="98693-133">S_OK</span></span> 
  
> <span data-ttu-id="98693-134">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="98693-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98693-135">注釈</span><span class="sxs-lookup"><span data-stu-id="98693-135">Remarks</span></span>

<span data-ttu-id="98693-136">MAPI は **、IMSLogon::OpenEntry** メソッドを呼び出して、メッセージ ストア内のフォルダーまたはメッセージを開きます。</span><span class="sxs-lookup"><span data-stu-id="98693-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="98693-137">MAPI は、開くオブジェクトのエントリ識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="98693-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="98693-138">メッセージ ストア プロバイダーは  _、lppUnk_ パラメーターで指定されたオブジェクトにさらにアクセスできるポインターを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="98693-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="98693-139">MAPI が **IMSLogon::OpenEntry** を呼び出す前に、指定されたメッセージまたはフォルダーエントリ識別子が、このメッセージ ストア プロバイダーによって登録された識別子と一致すると最初に判断されます。</span><span class="sxs-lookup"><span data-stu-id="98693-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="98693-140">ストア プロバイダーがエントリ識別子を登録する方法の詳細については [、「IMAPISupport::SetProviderUID」を参照してください](imapisupport-setprovideruid.md)。</span><span class="sxs-lookup"><span data-stu-id="98693-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="98693-141">**IMSLogon::OpenEntry** は、クライアントが **IMSLogon::OpenEntry** を呼び出さない以外は、メッセージ ストア オブジェクトの [IMsgStore::OpenEntry](imsgstore-openentry.md)メソッドと同じです。MAPI は **、IMAPISession::OpenEntry** メソッドを処理するときに **IMSLogon::OpenEntry を呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="98693-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="98693-142">**IMSLogon::OpenEntry** を使用して開くオブジェクトは、メッセージ ストア オブジェクトを使用して開いたオブジェクトとまったく同じように扱う必要があります。特に、この呼び出しを使用して開いたオブジェクトは、メッセージ ストア オブジェクトが解放されると無効になる必要があります。</span><span class="sxs-lookup"><span data-stu-id="98693-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="98693-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="98693-143">See also</span></span>



[<span data-ttu-id="98693-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="98693-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="98693-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="98693-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="98693-146">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="98693-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

