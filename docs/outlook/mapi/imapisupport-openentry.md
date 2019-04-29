---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cfbb799336aa1e75fa36e03e55d82c3af3409f10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409616"
---
# <a name="imapisupportopenentry"></a><span data-ttu-id="b6ca3-103">IMAPISupport::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b6ca3-103">IMAPISupport::OpenEntry</span></span>

  
  
<span data-ttu-id="b6ca3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6ca3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6ca3-105">オブジェクトを開き、さらにアクセスするためのインターフェイスポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-105">Opens an object and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="b6ca3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b6ca3-106">Parameters</span></span>

 <span data-ttu-id="b6ca3-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b6ca3-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b6ca3-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b6ca3-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="b6ca3-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b6ca3-110">順番開くオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="b6ca3-111">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="b6ca3-111">_lpInterface_</span></span>
  
> <span data-ttu-id="b6ca3-112">順番オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="b6ca3-113">返されるオブジェクトの標準インターフェイスで NULL 結果が渡されます。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-113">Passing NULL results in the object's standard interface being returned.</span></span> <span data-ttu-id="b6ca3-114">たとえば、開くオブジェクトがメッセージの場合、標準インターフェイスは[IMessage](imessageimapiprop.md)になります。フォルダーの場合は、 [imapifolder](imapifolderimapicontainer.md)です。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="b6ca3-115">アドレス帳オブジェクトの標準インターフェイスは、配布リストの[idistlist](idistlistimapicontainer.md)で、メッセージングユーザーの[idistlist](imailuserimapiprop.md)です。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="b6ca3-116">_ulo・フラグ_</span><span class="sxs-lookup"><span data-stu-id="b6ca3-116">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="b6ca3-117">順番オブジェクトを開く方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="b6ca3-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-118">The following flags can be set:</span></span>
    
<span data-ttu-id="b6ca3-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b6ca3-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="b6ca3-120">呼び出し元に対して許可されている最大のネットワークアクセス許可を使用して、オブジェクトを開くように要求します。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-120">Requests that the object be opened with the maximum network permissions allowed for the caller.</span></span> <span data-ttu-id="b6ca3-121">たとえば、呼び出し元に読み取り/書き込みアクセス許可が設定されている場合、オブジェクトは読み取り/書き込みとして開かれる必要があります。呼び出し元が読み取り専用のアクセス許可を持っている場合、そのオブジェクトは読み取り専用として開かれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-121">For example, if the caller has read/write permission, the object should be opened as read/write; if the caller has read-only permission, the object should be opened as read-only.</span></span> 
    
<span data-ttu-id="b6ca3-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b6ca3-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="b6ca3-123">オブジェクトが呼び出し元から完全にアクセス可能になる前に、 **openentry**が正常に返されることを許可します。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-123">Allows **OpenEntry** to return successfully, possibly before the object is fully accessible to the caller.</span></span> <span data-ttu-id="b6ca3-124">オブジェクトにアクセスできない場合は、その後のオブジェクト呼び出しでエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-124">If the object is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="b6ca3-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b6ca3-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="b6ca3-126">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-126">Requests read/write permission.</span></span> <span data-ttu-id="b6ca3-127">既定では、オブジェクトは読み取り専用として開かれ、読み取り/書き込みアクセス許可が付与されているという前提で呼び出し元は機能しません。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-127">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="b6ca3-128">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="b6ca3-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="b6ca3-129">読み上げ開かれているオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="b6ca3-130">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="b6ca3-130">_lppUnk_</span></span>
  
> <span data-ttu-id="b6ca3-131">読み上げ開かれているオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b6ca3-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="b6ca3-132">Return value</span></span>

<span data-ttu-id="b6ca3-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6ca3-133">S_OK</span></span> 
  
> <span data-ttu-id="b6ca3-134">オブジェクトが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="b6ca3-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b6ca3-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b6ca3-136">読み取り専用オブジェクトを変更しようとしたか、ユーザーが必要なアクセス許可を持っていないオブジェクトへのアクセスが行われました。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-136">An attempt was made to modify a read-only object, or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="b6ca3-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b6ca3-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b6ca3-138">_lな tryid_パラメーターに渡されたエントリ id に関連付けられたオブジェクトがありません。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-138">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="b6ca3-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b6ca3-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="b6ca3-140">_lな tryid_パラメーターで渡されたエントリ id は、認識できない形式です。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-140">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="b6ca3-141">通常、この値は、オブジェクトを含むアドレス帳プロバイダーが開かれていない場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-141">This value is typically returned if the address book provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b6ca3-142">注釈</span><span class="sxs-lookup"><span data-stu-id="b6ca3-142">Remarks</span></span>

<span data-ttu-id="b6ca3-143">**imapisupport:: openentry**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-143">The **IMAPISupport::OpenEntry** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="b6ca3-144">サービスプロバイダーは、 **imapisupport:: openentry**を呼び出して、特定のオブジェクトへのアクセスに使用できるインターフェイスへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-144">Service providers call **IMAPISupport::OpenEntry** to retrieve a pointer to an interface that can be used to access a particular object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b6ca3-145">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b6ca3-145">Notes to callers</span></span>

<span data-ttu-id="b6ca3-146">開こうとしているオブジェクトの種類がわからない場合は、 **imapisupport:: openentry**のみを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-146">Call **IMAPISupport::OpenEntry** only when you do not know what kind of object you are opening.</span></span> <span data-ttu-id="b6ca3-147">フォルダーまたはメッセージを開いていることがわかっている場合は、代わりに[IMsgStore:: openentry](imsgstore-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-147">If you know you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md) instead.</span></span> <span data-ttu-id="b6ca3-148">アドレス帳コンテナー、メッセージングユーザー、または配布リストを開いていることがわかっている場合は、 [IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-148">If you know you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="b6ca3-149">これらのより具体的な方法は、 **imapisupport:: openentry**よりも高速です。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-149">These more specific methods are faster than **IMAPISupport::OpenEntry**.</span></span> 
  
 <span data-ttu-id="b6ca3-150">**imapisupport:: openentry**は、 _ulflags_パラメーターに MAPI_MODIFY または MAPI_BEST_ACCESS フラグを設定し、アクセス許可が十分でない限り、すべてのオブジェクトを読み取り専用として開きます。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-150">**IMAPISupport::OpenEntry** opens all objects as read-only, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter and your permissions are sufficient.</span></span> <span data-ttu-id="b6ca3-151">これらのフラグのいずれかを設定しても、特定の種類のアクセス権は保証されません。付与されるアクセス許可は、そのオブジェクトを所有するアクセスレベル、オブジェクト、およびサービスプロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-151">Setting one of these flags does not guarantee a particular type of access; the permissions that you are granted depend on your access level, the object, and the service provider that owns the object.</span></span> <span data-ttu-id="b6ca3-152">開いているオブジェクトのアクセスレベルを確認するには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-152">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="b6ca3-153">_lpulobjtype_パラメーターで返された値を調べて、返されたオブジェクトの種類が期待したものであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-153">Check the value returned in the  _lpulObjType_ parameter to determine that the object type returned is what you expected.</span></span> <span data-ttu-id="b6ca3-154">オブジェクトの種類が想定どおりの場合は、ポインターを_lppunk_パラメーターから適切な型のポインターにキャストします。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-154">If the object type is as expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="b6ca3-155">たとえば、フォルダーを開いている場合は、LPMAPIFOLDER 型のポインターに_lppunk_をキャストします。</span><span class="sxs-lookup"><span data-stu-id="b6ca3-155">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b6ca3-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6ca3-156">See also</span></span>



[<span data-ttu-id="b6ca3-157">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6ca3-157">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

