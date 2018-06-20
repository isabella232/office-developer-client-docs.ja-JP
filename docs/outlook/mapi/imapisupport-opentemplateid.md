---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f99843bcdf3689acad72145a33d6a9804175a413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800785"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="1063f-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="1063f-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="1063f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1063f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1063f-105">外部のアドレス帳で受信者のエントリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1063f-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
```cpp
HRESULT OpenTemplateID(
ULONG cbTemplateID,
LPENTRYID lpTemplateID,
ULONG ulTemplateFlags,
LPMAPIPROP lpMAPIPropData,
LPCIID lpInterface,
LPMAPIPROP FAR * lppMAPIPropNew,
LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a><span data-ttu-id="1063f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1063f-106">Parameters</span></span>

 <span data-ttu-id="1063f-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="1063f-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="1063f-108">[in]_LpTemplateID_で示されるテンプレート識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="1063f-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="1063f-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="1063f-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="1063f-110">[in]テンプレート識別子を開くには、受信者のエントリの**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1063f-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="1063f-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="1063f-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="1063f-112">[in]エントリを開く方法について説明するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="1063f-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="1063f-113">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1063f-113">The following flag can be set:</span></span>
    
<span data-ttu-id="1063f-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="1063f-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="1063f-115">新しいエントリを作成しています。</span><span class="sxs-lookup"><span data-stu-id="1063f-115">A new entry is being created.</span></span> <span data-ttu-id="1063f-116">_LpMAPIPropData_パラメーターによって、または特定のインターフェイスを返すことによって示されるプロパティを変更することにより、エントリを作成する方法が制御できる外部のプロバイダーでは、MAPI から[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)の後続の呼び出しを受信したとき新しいエントリのプロパティを設定する方法を制御するのには_lppMAPIPropNew_で実装します。</span><span class="sxs-lookup"><span data-stu-id="1063f-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="1063f-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="1063f-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="1063f-118">[in]エントリにアクセスするのには、呼び出し元を使用するインターフェイスの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1063f-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="1063f-119">これは、外部のプロバイダーは独自の実装をラップし、 _lppMAPIPropNew_パラメーターに返すの実装です。</span><span class="sxs-lookup"><span data-stu-id="1063f-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="1063f-120">_LpMAPIPropData_パラメーターは、読み取り/書き込みインタ フェースの実装から派生する] をポイントする必要があります[IMAPIProp: IUnknown](imapipropiunknown.md) 、 _lpInterface_パラメーターで要求されたインターフェイスをサポートしているとします。</span><span class="sxs-lookup"><span data-stu-id="1063f-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="1063f-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1063f-121">_lpInterface_</span></span>
  
> <span data-ttu-id="1063f-122">[in]エントリにアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1063f-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="1063f-123">_LppMAPIPropNew_パラメーターは、 _lpInterface_によって指定された型のインターフェイスを指します。</span><span class="sxs-lookup"><span data-stu-id="1063f-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="1063f-124">NULL を渡すことは、IID_IMailUser、メッセージング ユーザーのための標準インターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="1063f-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="1063f-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="1063f-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="1063f-126">[out]エントリにアクセスするため、外部のプロバイダーが提供するインターフェイスの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1063f-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="1063f-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="1063f-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="1063f-128">予約されています。NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1063f-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1063f-129">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1063f-129">Return value</span></span>

<span data-ttu-id="1063f-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="1063f-130">S_OK</span></span> 
  
> <span data-ttu-id="1063f-131">バインド処理が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="1063f-131">The binding process was successful.</span></span>
    
<span data-ttu-id="1063f-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1063f-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="1063f-133">外部のアドレス帳プロバイダーが存在しません。</span><span class="sxs-lookup"><span data-stu-id="1063f-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1063f-134">備考</span><span class="sxs-lookup"><span data-stu-id="1063f-134">Remarks</span></span>

<span data-ttu-id="1063f-135">**IMAPISupport::OpenTemplateID**メソッドは、アドレス帳プロバイダーのサポートのオブジェクトに対してのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="1063f-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="1063f-136">**OpenTemplateID**は、他のアドレス帳プロバイダーとも呼ばれる外部プロバイダーに属しているエントリのホストとして機能する、アドレス帳プロバイダーによってのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1063f-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="1063f-137">ホスト プロバイダーは、ホスト プロバイダー内のデータが外部のプロバイダーのコードにバインドされている場合に発生する、外部のエントリを開くには、 **OpenTemplateID**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1063f-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1063f-138">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1063f-138">Notes to callers</span></span>

<span data-ttu-id="1063f-139">外部のアドレス帳プロバイダーからのテンプレートの識別子を持つエントリの保存をサポートする場合にのみ、 **OpenTemplateID**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1063f-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="1063f-140">このようなサポートは、 [IABContainer::CreateEntry](iabcontainer-createentry.md)と[IABLogon::OpenEntry](iablogon-openentry.md)の実装に追加の要件を配置します。</span><span class="sxs-lookup"><span data-stu-id="1063f-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="1063f-141">詳細については、これらのメソッドと[ホストのアドレス帳プロバイダーとしての機能](acting-as-a-host-address-book-provider.md)の説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1063f-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="1063f-142">渡された同じプロパティ オブジェクトの実装、バインドされたインターフェイスと**OpenTemplateID**の呼び出しが返された場合、オブジェクトへの参照、プロパティをリリースできます。</span><span class="sxs-lookup"><span data-stu-id="1063f-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="1063f-143">外部プロバイダーが独自の参照を保持するオブジェクトの**AddRef**メソッドを呼び出すためにです。</span><span class="sxs-lookup"><span data-stu-id="1063f-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="1063f-144">外部プロバイダーがプロパティ オブジェクトへの参照を保持する必要がない場合**OpenTemplateID**は、プロパティがバインドされていないオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="1063f-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="1063f-145">**OpenTemplateID**では、MAPI_E_UNKNOWN_ENTRYID が失敗した場合、読み取り専用で、エントリを処理することで継続してみてください。</span><span class="sxs-lookup"><span data-stu-id="1063f-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1063f-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="1063f-146">See also</span></span>



[<span data-ttu-id="1063f-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="1063f-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="1063f-148">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1063f-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="1063f-149">PidTagTemplateid の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="1063f-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="1063f-150">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1063f-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

