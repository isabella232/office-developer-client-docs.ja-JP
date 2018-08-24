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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bf6386ae3a7d835c8748e332235d8737c7a502e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589470"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="eecb3-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="eecb3-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="eecb3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eecb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eecb3-105">コンテナー、ユーザー、または配布リストにメッセージを開き、さらにアクセスを提供するインターフェイスの実装にポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="eecb3-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="eecb3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="eecb3-106">Parameters</span></span>

 <span data-ttu-id="eecb3-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="eecb3-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="eecb3-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="eecb3-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="eecb3-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="eecb3-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="eecb3-110">[in]メッセージングのユーザー、または配布リストを開き、コンテナーのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="eecb3-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="eecb3-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="eecb3-111">_lpInterface_</span></span>
  
> <span data-ttu-id="eecb3-112">[in]開いているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="eecb3-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="eecb3-113">NULL を渡すことは、オブジェクトの標準的なインタ フェースの識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="eecb3-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="eecb3-114">コンテナーでは、標準のインタ フェースは[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="eecb3-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="eecb3-115">標準インターフェイスを使用しているアドレス帳オブジェクト[IDistList: IMAPIContainer](idistlistimapicontainer.md)の配布リストと[IMailUser: IMAPIProp](imailuserimapiprop.md)メッセージング ユーザーのです。</span><span class="sxs-lookup"><span data-stu-id="eecb3-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="eecb3-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eecb3-116">_ulFlags_</span></span>
  
> <span data-ttu-id="eecb3-117">[in]オブジェクトを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="eecb3-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="eecb3-118">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="eecb3-118">The following flags can be set:</span></span>
    
<span data-ttu-id="eecb3-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="eecb3-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="eecb3-120">ユーザーおよび最大のクライアント アプリケーションへのアクセスに使用される最大ネットワークのアクセス許可を持つオブジェクトを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="eecb3-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="eecb3-121">たとえば、クライアントに読み取り/書き込み権限がある場合、オブジェクト開く必要があります読み取り/書き込みアクセス許可を持つクライアントに読み取り専用のアクセス許可がある場合は、読み取り専用権限を持つオブジェクトを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="eecb3-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="eecb3-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="eecb3-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="eecb3-123">**OpenEntry**メソッドが正常に完了、可能性のある呼び出し元のクライアントが完全にオブジェクトを利用する前にすることができます。</span><span class="sxs-lookup"><span data-stu-id="eecb3-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="eecb3-124">オブジェクト アクセスできない場合は、後続のオブジェクトの呼び出しを実行するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="eecb3-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="eecb3-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="eecb3-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="eecb3-126">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="eecb3-126">Requests read/write permission.</span></span> <span data-ttu-id="eecb3-127">既定では、読み取り専用のアクセス権を持つオブジェクトが開いているし、クライアントの読み取り/書き込み権限が付与されていると仮定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eecb3-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="eecb3-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="eecb3-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="eecb3-129">[out]開かれたオブジェクトの型へのポインター。</span><span class="sxs-lookup"><span data-stu-id="eecb3-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="eecb3-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="eecb3-130">_lppUnk_</span></span>
  
> <span data-ttu-id="eecb3-131">[out]開かれたオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="eecb3-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eecb3-132">注釈</span><span class="sxs-lookup"><span data-stu-id="eecb3-132">Remarks</span></span>

<span data-ttu-id="eecb3-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="eecb3-133">S_OK</span></span> 
  
> <span data-ttu-id="eecb3-134">オブジェクトが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="eecb3-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="eecb3-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="eecb3-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="eecb3-136">ユーザーには十分なアクセス許可、オブジェクトを開くか、読み取り/書き込みアクセス許可を持つ読み取り専用オブジェクトを開くしようとしました。</span><span class="sxs-lookup"><span data-stu-id="eecb3-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="eecb3-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="eecb3-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="eecb3-138">_LpEntryID_で指定されたエントリの識別子は、オブジェクトを表していません。</span><span class="sxs-lookup"><span data-stu-id="eecb3-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="eecb3-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="eecb3-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="eecb3-140">_LpEntryID_パラメーターのエントリ id がアドレス帳プロバイダーで認識される形式ではありません。</span><span class="sxs-lookup"><span data-stu-id="eecb3-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="eecb3-141">注釈</span><span class="sxs-lookup"><span data-stu-id="eecb3-141">Remarks</span></span>

<span data-ttu-id="eecb3-142">MAPI では、ユーザー、または配布リストにメッセージを開くには、コンテナーでは、 **OpenEntry**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eecb3-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="eecb3-143">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="eecb3-143">Notes to implementers</span></span>

<span data-ttu-id="eecb3-144">MAPI の**OpenEntry**メソッドを呼び出すと、前にして、別のプロバイダーに、 _lpEntryID_パラメーターのエントリの識別子が属していることを決定します。</span><span class="sxs-lookup"><span data-stu-id="eecb3-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="eecb3-145">MAPI は、メソッドを呼び出して、 [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)の起動時に登録した**MAPIUID**のエントリの識別子では、 [MAPIUID](mapiuid.md)構造を照合することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="eecb3-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="eecb3-146">_UlFlags_パラメーターで、MAPI_MODIFY フラグまたは MAPI_BEST_ACCESS フラグが設定されていない場合は、読み取り専用としてオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="eecb3-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="eecb3-147">要求されたオブジェクトの変更を許可しない場合はすべてのオブジェクトを開くされず、MAPI_E_NO_ACCESS を返します。</span><span class="sxs-lookup"><span data-stu-id="eecb3-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="eecb3-148">MAPI では、 _lpEntryID_に NULL が成功した場合は、コンテナー階層のルート コンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="eecb3-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="eecb3-149">別のプロバイダーからコピーしたオブジェクトを開くにが求められているオブジェクトがあります。</span><span class="sxs-lookup"><span data-stu-id="eecb3-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="eecb3-150">この例では、 **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="eecb3-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="eecb3-151">オブジェクトはこのプロパティをサポートしている場合は、外部のプロバイダーでは、 _lpTemplateID_パラメーターで 0 _ulTemplateFlags の**PR_TEMPLATEID**を渡すことでこの記事のコードにバインドする[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出す_パラメーター。</span><span class="sxs-lookup"><span data-stu-id="eecb3-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="eecb3-152">**IMAPISupport::OpenTemplateID**は、この情報を外部のプロバイダーの[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)メソッドの呼び出しで外部プロバイダーに渡します。</span><span class="sxs-lookup"><span data-stu-id="eecb3-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="eecb3-153">**IMAPISupport::OpenTemplateID**では、エラーが発生した場合は、通常外部プロバイダーが使用できない場合や、プロファイルに含まれていませんので続行しようと読み取り専用で非連結のエントリを処理することによって。</span><span class="sxs-lookup"><span data-stu-id="eecb3-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="eecb3-154">外部アドレス帳のエントリを開く方法の詳細については、[ホストのアドレス帳プロバイダーとしての機能](acting-as-a-host-address-book-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eecb3-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eecb3-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="eecb3-155">See also</span></span>



[<span data-ttu-id="eecb3-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eecb3-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

