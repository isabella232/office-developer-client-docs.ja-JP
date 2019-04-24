---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348938"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="6aa96-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6aa96-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="6aa96-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6aa96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6aa96-105">コンテナー、メッセージングユーザー、または配布リストを開き、インターフェイス実装へのポインターを返して、さらにアクセスできるようにします。</span><span class="sxs-lookup"><span data-stu-id="6aa96-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="6aa96-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6aa96-106">Parameters</span></span>

 <span data-ttu-id="6aa96-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6aa96-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="6aa96-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="6aa96-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6aa96-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="6aa96-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="6aa96-110">順番開くコンテナー、メッセージングユーザー、または配布リストのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6aa96-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="6aa96-111">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="6aa96-111">_lpInterface_</span></span>
  
> <span data-ttu-id="6aa96-112">順番開いているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6aa96-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="6aa96-113">NULL を渡すと、オブジェクトの標準インターフェイスの識別子が返されます。</span><span class="sxs-lookup"><span data-stu-id="6aa96-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="6aa96-114">コンテナーの場合、標準インターフェイスは[IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)です。</span><span class="sxs-lookup"><span data-stu-id="6aa96-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="6aa96-115">アドレス帳オブジェクトの標準インターフェイスは[idistlist: IMAPIContainer](idistlistimapicontainer.md)の配布リストと[idistlist: imapiprop](imailuserimapiprop.md)がメッセージングユーザーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="6aa96-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="6aa96-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6aa96-116">_ulFlags_</span></span>
  
> <span data-ttu-id="6aa96-117">順番オブジェクトを開く方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="6aa96-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="6aa96-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6aa96-118">The following flags can be set:</span></span>
    
<span data-ttu-id="6aa96-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6aa96-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="6aa96-120">ユーザーに対して許可される最大のネットワークアクセス許可と、クライアントアプリケーションの最大アクセス権を使用して、オブジェクトを開くように要求します。</span><span class="sxs-lookup"><span data-stu-id="6aa96-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="6aa96-121">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、読み取り/書き込みアクセス許可を使用してオブジェクトを開く必要があります。クライアントが読み取り専用アクセス許可を持っている場合、そのオブジェクトは読み取り専用アクセス許可で開かれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6aa96-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="6aa96-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6aa96-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="6aa96-123">**openentry**メソッドを正常に返すことができるようにします。これは、呼び出し元クライアントが完全にオブジェクトにアクセスする前である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6aa96-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="6aa96-124">オブジェクトがアクセスされていない場合は、その後のオブジェクト呼び出しでエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="6aa96-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="6aa96-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6aa96-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="6aa96-126">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="6aa96-126">Requests read/write permission.</span></span> <span data-ttu-id="6aa96-127">既定では、オブジェクトは読み取り専用アクセスで開かれ、クライアントは読み取り/書き込みアクセス許可が与えられていると想定することはできません。</span><span class="sxs-lookup"><span data-stu-id="6aa96-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="6aa96-128">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="6aa96-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="6aa96-129">読み上げ開かれているオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6aa96-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="6aa96-130">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="6aa96-130">_lppUnk_</span></span>
  
> <span data-ttu-id="6aa96-131">読み上げ開かれているオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6aa96-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6aa96-132">解説</span><span class="sxs-lookup"><span data-stu-id="6aa96-132">Remarks</span></span>

<span data-ttu-id="6aa96-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="6aa96-133">S_OK</span></span> 
  
> <span data-ttu-id="6aa96-134">オブジェクトが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="6aa96-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="6aa96-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6aa96-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6aa96-136">ユーザーがオブジェクトを開くための十分な権限を持っていないか、読み取り/書き込みアクセス許可を持つ読み取り専用オブジェクトを開こうとしました。</span><span class="sxs-lookup"><span data-stu-id="6aa96-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="6aa96-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6aa96-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6aa96-138">_lな tryid_で指定されたエントリ識別子は、オブジェクトを表していません。</span><span class="sxs-lookup"><span data-stu-id="6aa96-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="6aa96-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6aa96-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="6aa96-140">_lな tryid_パラメーターのエントリ id は、アドレス帳プロバイダーで認識される形式ではありません。</span><span class="sxs-lookup"><span data-stu-id="6aa96-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6aa96-141">解説</span><span class="sxs-lookup"><span data-stu-id="6aa96-141">Remarks</span></span>

<span data-ttu-id="6aa96-142">MAPI は**openentry**メソッドを呼び出して、コンテナー、メッセージングユーザー、または配布リストを開きます。</span><span class="sxs-lookup"><span data-stu-id="6aa96-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6aa96-143">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="6aa96-143">Notes to implementers</span></span>

<span data-ttu-id="6aa96-144">MAPI は、 **openentry**メソッドを呼び出す前に、 _lpentryid_パラメーターのエントリ識別子が自分に属していること、および別のプロバイダーには属していないことを判断します。</span><span class="sxs-lookup"><span data-stu-id="6aa96-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="6aa96-145">MAPI では、エントリ識別子の[MAPIUID](mapiuid.md)構造を、起動時に[imapisupport:: setprovideruid](imapisupport-setprovideruid.md)メソッドを呼び出すことによって登録した**MAPIUID**と照合することによって、これを行います。</span><span class="sxs-lookup"><span data-stu-id="6aa96-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="6aa96-146">_ulflags_パラメーターに MAPI_MODIFY または MAPI_BEST_ACCESS フラグが設定されていない場合は、オブジェクトを読み取り専用として開きます。</span><span class="sxs-lookup"><span data-stu-id="6aa96-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="6aa96-147">要求されたオブジェクトの変更が許可されていない場合は、オブジェクトを開かずに MAPI_E_NO_ACCESS を返します。</span><span class="sxs-lookup"><span data-stu-id="6aa96-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="6aa96-148">MAPI が_lな tryid_に対して NULL を渡す場合は、コンテナー階層のルートコンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="6aa96-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="6aa96-149">開くように求められているオブジェクトは、別のプロバイダーからコピーされたオブジェクトである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6aa96-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="6aa96-150">この場合は、 **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6aa96-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="6aa96-151">オブジェクトがこのプロパティをサポートしている場合は、 [imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出して、外部プロバイダーのこのエントリのコードにバインドし、 _lpTemplateID_パラメーターで**PR_TEMPLATEID**を渡し、ultemplateflags では0にします。 __ パラメーター。</span><span class="sxs-lookup"><span data-stu-id="6aa96-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="6aa96-152">**imapisupport:: OpenTemplateID**は、外部プロバイダーの[IABLogon:: OpenTemplateID](iablogon-opentemplateid.md)メソッドへの呼び出しで、この情報を外部プロバイダーに渡します。</span><span class="sxs-lookup"><span data-stu-id="6aa96-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="6aa96-153">**imapisupport:: OpenTemplateID**がエラーを発生させる場合は、通常、外部プロバイダーが使用できないか、プロファイルに含まれていないため、非連結エントリを読み取り専用として処理することによって処理を続行します。</span><span class="sxs-lookup"><span data-stu-id="6aa96-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="6aa96-154">外部アドレス帳エントリを開く方法の詳細については、「[ホストアドレス帳プロバイダーとして機能する](acting-as-a-host-address-book-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6aa96-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6aa96-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="6aa96-155">See also</span></span>



[<span data-ttu-id="6aa96-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6aa96-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

