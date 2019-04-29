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
# <a name="imslogonopenentry"></a><span data-ttu-id="c51cc-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c51cc-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="c51cc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c51cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c51cc-105">folder オブジェクトまたは message オブジェクトを開き、オブジェクトへのポインターを返します。これにより、さらにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="c51cc-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="c51cc-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c51cc-106">Parameters</span></span>

 <span data-ttu-id="c51cc-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c51cc-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c51cc-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="c51cc-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c51cc-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="c51cc-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c51cc-110">順番開くフォルダーまたはメッセージオブジェクトのエントリ id のアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c51cc-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="c51cc-111">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="c51cc-111">_lpInterface_</span></span>
  
> <span data-ttu-id="c51cc-112">順番オブジェクトのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c51cc-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="c51cc-113">NULL を渡すことは、オブジェクトがそのようなオブジェクトの標準インターフェイスにキャストされることを示します。</span><span class="sxs-lookup"><span data-stu-id="c51cc-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="c51cc-114">_lpinterface_パラメーターは、オブジェクトの適切なインターフェイスの識別子に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="c51cc-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="c51cc-115">_ulo・フラグ_</span><span class="sxs-lookup"><span data-stu-id="c51cc-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="c51cc-116">順番オブジェクトを開く方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c51cc-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="c51cc-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c51cc-117">The following flags can be set:</span></span>
    
<span data-ttu-id="c51cc-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c51cc-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="c51cc-119">このオブジェクトは、ユーザーに対して許可されている最大アクセス許可と、クライアントアプリケーションの最大アクセス許可を使用して開かれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c51cc-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="c51cc-120">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合、オブジェクトは読み取り/書き込みアクセス許可で開かれます。クライアントが読み取り専用アクセス許可を持っている場合、そのオブジェクトは読み取り専用アクセス許可で開かれます。</span><span class="sxs-lookup"><span data-stu-id="c51cc-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="c51cc-121">クライアントは、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得することによってアクセス許可レベルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="c51cc-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="c51cc-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c51cc-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c51cc-123">呼び出し元のオブジェクトが呼び出し元のアプリケーションで使用できない場合でも、呼び出しを成功させることができます。</span><span class="sxs-lookup"><span data-stu-id="c51cc-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="c51cc-124">オブジェクトを使用できない場合は、その後のオブジェクトへの呼び出しでエラーが返されることがあります。</span><span class="sxs-lookup"><span data-stu-id="c51cc-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="c51cc-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="c51cc-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="c51cc-126">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="c51cc-126">Requests read/write permission.</span></span> <span data-ttu-id="c51cc-127">既定では、オブジェクトは読み取り専用のアクセス許可で作成され、読み取り/書き込みアクセス許可が付与されているという前提でクライアントを動作させることはできません。</span><span class="sxs-lookup"><span data-stu-id="c51cc-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="c51cc-128">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="c51cc-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="c51cc-129">読み上げ開かれているオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c51cc-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="c51cc-130">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="c51cc-130">_lppUnk_</span></span>
  
> <span data-ttu-id="c51cc-131">読み上げ開かれているオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c51cc-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c51cc-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="c51cc-132">Return value</span></span>

<span data-ttu-id="c51cc-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="c51cc-133">S_OK</span></span> 
  
> <span data-ttu-id="c51cc-134">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c51cc-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c51cc-135">注釈</span><span class="sxs-lookup"><span data-stu-id="c51cc-135">Remarks</span></span>

<span data-ttu-id="c51cc-136">MAPI は**IMSLogon:: openentry**メソッドを呼び出して、メッセージストア内のフォルダーまたはメッセージを開きます。</span><span class="sxs-lookup"><span data-stu-id="c51cc-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="c51cc-137">MAPI は、開くオブジェクトのエントリ識別子に渡されます。</span><span class="sxs-lookup"><span data-stu-id="c51cc-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="c51cc-138">メッセージストアプロバイダーは、 _lppunk_パラメーターで指定されたオブジェクトへのアクセスを可能にするポインターを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c51cc-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="c51cc-139">MAPI が**IMSLogon:: openentry**を呼び出す前に、まず、指定されたメッセージまたはフォルダーのエントリ id がこのメッセージストアプロバイダーによって登録されたものと一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="c51cc-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="c51cc-140">ストアプロバイダーがエントリ識別子を登録する方法の詳細については、「 [imapisupport:: setprovideruid](imapisupport-setprovideruid.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c51cc-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="c51cc-141">**IMSLogon:: openentry**は、メッセージストアオブジェクトの[IMsgStore:: openentry](imsgstore-openentry.md)メソッドと同じですが、クライアントが**IMSLogon:: openentry**を呼び出さない点が異なります。MAPI は、 **imapisession:: openentry**メソッドを処理するときに**IMSLogon:: openentry**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c51cc-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="c51cc-142">**IMSLogon:: openentry**を使用して開いたオブジェクトは、メッセージストアオブジェクトを使用して開かれたオブジェクトとまったく同じように処理される必要があります。特に、メッセージストアオブジェクトが解放されると、この呼び出しを使用して開かれたオブジェクトは無効になります。</span><span class="sxs-lookup"><span data-stu-id="c51cc-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c51cc-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="c51cc-143">See also</span></span>



[<span data-ttu-id="c51cc-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="c51cc-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="c51cc-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c51cc-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="c51cc-146">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c51cc-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

