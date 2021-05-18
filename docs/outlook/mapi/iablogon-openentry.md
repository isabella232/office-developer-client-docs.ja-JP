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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409231"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="5589a-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5589a-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="5589a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5589a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5589a-105">コンテナー、メッセージング ユーザー、または配布リストを開き、インターフェイス実装へのポインターを返して、さらにアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="5589a-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="5589a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5589a-106">Parameters</span></span>

 <span data-ttu-id="5589a-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5589a-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="5589a-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="5589a-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5589a-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5589a-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="5589a-110">[in]開くコンテナー、メッセージング ユーザー、または配布リストのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5589a-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="5589a-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5589a-111">_lpInterface_</span></span>
  
> <span data-ttu-id="5589a-112">[in]開いているオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5589a-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="5589a-113">NULL を渡す場合は、オブジェクトの標準インターフェイスの識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="5589a-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="5589a-114">コンテナーの場合、標準インターフェイスは [IABContainer : IMAPIContainer です](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="5589a-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="5589a-115">アドレス帳オブジェクトの標準インターフェイスは、配布リストの [IDistList : IMAPIContainer、](idistlistimapicontainer.md) メッセージング ユーザーの [IMailUser : IMAPIProp](imailuserimapiprop.md) です。</span><span class="sxs-lookup"><span data-stu-id="5589a-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="5589a-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5589a-116">_ulFlags_</span></span>
  
> <span data-ttu-id="5589a-117">[in]オブジェクトの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5589a-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="5589a-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5589a-118">The following flags can be set:</span></span>
    
<span data-ttu-id="5589a-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5589a-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="5589a-120">ユーザーに許可される最大ネットワークアクセス許可と最大クライアント アプリケーション アクセス権を使用してオブジェクトを開く要求。</span><span class="sxs-lookup"><span data-stu-id="5589a-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="5589a-121">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、オブジェクトを読み取り/書き込みアクセス許可で開く必要があります。クライアントに読み取り専用のアクセス許可がある場合は、オブジェクトを読み取り専用のアクセス許可で開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="5589a-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="5589a-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5589a-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5589a-123">呼び出し元のクライアントがオブジェクトに完全にアクセスする前に **、OpenEntry** メソッドが正常に返されます。</span><span class="sxs-lookup"><span data-stu-id="5589a-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="5589a-124">オブジェクトにアクセスしない場合、後続のオブジェクト呼び出しを実行するとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5589a-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="5589a-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5589a-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="5589a-126">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="5589a-126">Requests read/write permission.</span></span> <span data-ttu-id="5589a-127">既定では、オブジェクトは読み取り専用アクセス権で開かれません。クライアントは、読み取り/書き込みアクセス許可が付与されたと想定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5589a-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="5589a-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="5589a-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="5589a-129">[out]開いたオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5589a-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="5589a-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="5589a-130">_lppUnk_</span></span>
  
> <span data-ttu-id="5589a-131">[out]開いたオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5589a-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5589a-132">注釈</span><span class="sxs-lookup"><span data-stu-id="5589a-132">Remarks</span></span>

<span data-ttu-id="5589a-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="5589a-133">S_OK</span></span> 
  
> <span data-ttu-id="5589a-134">オブジェクトが正常に開かされました。</span><span class="sxs-lookup"><span data-stu-id="5589a-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="5589a-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5589a-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="5589a-136">ユーザーがオブジェクトを開くアクセス許可が不足しているか、読み取り/書き込みアクセス許可を持つ読み取り専用オブジェクトを開く試み。</span><span class="sxs-lookup"><span data-stu-id="5589a-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="5589a-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5589a-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5589a-138">_lpEntryID で指定されたエントリ識別子は_、オブジェクトを表すではありません。</span><span class="sxs-lookup"><span data-stu-id="5589a-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="5589a-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5589a-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="5589a-140">_lpEntryID_ パラメーターのエントリ識別子は、アドレス帳プロバイダーによって認識される形式ではありません。</span><span class="sxs-lookup"><span data-stu-id="5589a-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5589a-141">注釈</span><span class="sxs-lookup"><span data-stu-id="5589a-141">Remarks</span></span>

<span data-ttu-id="5589a-142">MAPI は **OpenEntry メソッドを呼** び出して、コンテナー、メッセージング ユーザー、または配布リストを開きます。</span><span class="sxs-lookup"><span data-stu-id="5589a-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5589a-143">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="5589a-143">Notes to implementers</span></span>

<span data-ttu-id="5589a-144">MAPI が **OpenEntry** メソッドを呼び出す前に  _、lpEntryID_ パラメーターのエントリ識別子がユーザーに属し、別のプロバイダーに属していないと判断します。</span><span class="sxs-lookup"><span data-stu-id="5589a-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="5589a-145">MAPI は、エントリ識別子の [MAPIUID](mapiuid.md)構造を、起動時に [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出して登録した **MAPIUID** と照合することでこれを行います。</span><span class="sxs-lookup"><span data-stu-id="5589a-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="5589a-146">_ulFlags_ パラメーターで MAPI_MODIFYまたはMAPI_BEST_ACCESSを設定しない限り、オブジェクトを読み取り専用として開きます。</span><span class="sxs-lookup"><span data-stu-id="5589a-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="5589a-147">要求されたオブジェクトの変更を許可しない場合は、オブジェクトを一向に開かMAPI_E_NO_ACCESS。</span><span class="sxs-lookup"><span data-stu-id="5589a-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="5589a-148">MAPI が  _lpEntryID_ に NULL を渡す場合は、コンテナー階層でルート コンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="5589a-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="5589a-149">開く必要があるオブジェクトは、別のプロバイダーからコピーされたオブジェクトである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5589a-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="5589a-150">この場合、このプロパティは PR_TEMPLATEID **(** [PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="5589a-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="5589a-151">オブジェクトがこのプロパティをサポートしている場合は [、IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出して、外部プロバイダーのこのエントリのコードにバインドし _、lpTemplateID_ パラメーターに _PR_TEMPLATEID、ulTemplateFlags_ パラメーターに 0 を渡します。 </span><span class="sxs-lookup"><span data-stu-id="5589a-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="5589a-152">**IMAPISupport::OpenTemplateID** は、外部プロバイダーの [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) メソッドへの呼び出しで、この情報を外部プロバイダーに渡します。</span><span class="sxs-lookup"><span data-stu-id="5589a-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="5589a-153">**IMAPISupport::OpenTemplateID** がエラーを発生する場合は、通常、外部プロバイダーが使用できないか、プロファイルに含まれていないため、非送信エントリを読み取り専用として扱って続行してください。</span><span class="sxs-lookup"><span data-stu-id="5589a-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="5589a-154">外部アドレス帳エントリを開く方法の詳細については、「ホスト アドレス帳プロバイダーとして機能する」 [を参照してください](acting-as-a-host-address-book-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="5589a-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5589a-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="5589a-155">See also</span></span>



[<span data-ttu-id="5589a-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5589a-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

