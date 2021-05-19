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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418506"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="422e5-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="422e5-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="422e5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="422e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="422e5-105">外部アドレス帳プロバイダーで受信者エントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="422e5-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="422e5-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="422e5-106">Parameters</span></span>

 <span data-ttu-id="422e5-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="422e5-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="422e5-108">[in]  _lpTemplateID_ が指すテンプレート識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="422e5-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="422e5-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="422e5-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="422e5-110">[in]開く受信者エントリの **テンプレート** PR_TEMPLATEID ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="422e5-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="422e5-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="422e5-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="422e5-112">[in]エントリを開く方法を説明するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="422e5-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="422e5-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="422e5-113">The following flag can be set:</span></span>
    
<span data-ttu-id="422e5-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="422e5-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="422e5-115">新しいエントリが作成されています。</span><span class="sxs-lookup"><span data-stu-id="422e5-115">A new entry is being created.</span></span> <span data-ttu-id="422e5-116">外部プロバイダーは、後続の [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) 呼び出しを MAPI から受信すると  _、lpMAPIPropData_ パラメーターが指すプロパティを変更するか  _、lppMAPIPropNew_ で特定のインターフェイス実装を返して、新しいエントリのプロパティを設定する方法を制御することで、エントリの作成方法を制御できます。</span><span class="sxs-lookup"><span data-stu-id="422e5-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="422e5-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="422e5-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="422e5-118">[in]呼び出し元がエントリへのアクセスに使用するインターフェイス実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="422e5-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="422e5-119">これは、外部プロバイダーが独自の実装でラップし  _、lppMAPIPropNew_ パラメーターに戻す実装です。</span><span class="sxs-lookup"><span data-stu-id="422e5-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="422e5-120">_lpMAPIPropData_ パラメーターは [、IMAPIProp : IUnknown](imapipropiunknown.md)から派生し _、lpInterface_ パラメーターで要求されるインターフェイスをサポートする読み取り/書き込みインターフェイス実装を指している必要があります。</span><span class="sxs-lookup"><span data-stu-id="422e5-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="422e5-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="422e5-121">_lpInterface_</span></span>
  
> <span data-ttu-id="422e5-122">[in]エントリへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="422e5-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="422e5-123">_lppMAPIPropNew_ パラメーターは _、lpInterface_ で指定された型のインターフェイスをポイントします。</span><span class="sxs-lookup"><span data-stu-id="422e5-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="422e5-124">NULL を渡すと、メッセージング ユーザーの標準インターフェイスが返IID_IMailUser。</span><span class="sxs-lookup"><span data-stu-id="422e5-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="422e5-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="422e5-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="422e5-126">[out]外部プロバイダーがエントリにアクセスするために提供するインターフェイス実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="422e5-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="422e5-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="422e5-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="422e5-128">予約済み。NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="422e5-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="422e5-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="422e5-129">Return value</span></span>

<span data-ttu-id="422e5-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="422e5-130">S_OK</span></span> 
  
> <span data-ttu-id="422e5-131">バインド プロセスが成功しました。</span><span class="sxs-lookup"><span data-stu-id="422e5-131">The binding process was successful.</span></span>
    
<span data-ttu-id="422e5-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="422e5-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="422e5-133">外部アドレス帳プロバイダーが存在しません。</span><span class="sxs-lookup"><span data-stu-id="422e5-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="422e5-134">注釈</span><span class="sxs-lookup"><span data-stu-id="422e5-134">Remarks</span></span>

<span data-ttu-id="422e5-135">**IMAPISupport::OpenTemplateID** メソッドは、アドレス帳プロバイダーのサポート オブジェクトにのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="422e5-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="422e5-136">**OpenTemplateID** は、他のアドレス帳プロバイダー (外部プロバイダーとも呼ばれる) に属するエントリのホストとして機能できるアドレス帳プロバイダーによってのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="422e5-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="422e5-137">ホスト プロバイダーは **OpenTemplateID** を呼び出して外部エントリを開きます。これは、ホスト プロバイダーのデータが外部プロバイダーのコードにバインドされている場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="422e5-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="422e5-138">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="422e5-138">Notes to callers</span></span>

<span data-ttu-id="422e5-139">**OpenTemplateID を呼** び出すのは、外部アドレス帳プロバイダーからのテンプレート識別子を持つエントリの格納をサポートしている場合のみです。</span><span class="sxs-lookup"><span data-stu-id="422e5-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="422e5-140">このようなサポートは [、IABContainer::CreateEntry](iabcontainer-createentry.md) および [IABLogon::OpenEntry 実装](iablogon-openentry.md) に追加の要件を設定します。</span><span class="sxs-lookup"><span data-stu-id="422e5-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="422e5-141">詳細については、これらのメソッドの説明とホスト アドレス帳プロバイダーとしての機能を [参照してください](acting-as-a-host-address-book-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="422e5-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="422e5-142">**OpenTemplateID 呼** び出しがバインド インターフェイスとして返される場合は、渡したのと同じプロパティ オブジェクト実装を使用して、プロパティ オブジェクトへの参照を解放できます。</span><span class="sxs-lookup"><span data-stu-id="422e5-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="422e5-143">これは、外部プロバイダーが独自の参照を保持するためにオブジェクトの **AddRef** メソッドを呼び出したためです。</span><span class="sxs-lookup"><span data-stu-id="422e5-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="422e5-144">外部プロバイダーがプロパティ オブジェクトへの参照を保持する必要が無い場合 **、OpenTemplateID** はアンバウンド プロパティ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="422e5-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="422e5-145">**OpenTemplateID に** エラーがMAPI_E_UNKNOWN_ENTRYID場合は、エントリを読み取り専用として扱って続行してください。</span><span class="sxs-lookup"><span data-stu-id="422e5-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="422e5-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="422e5-146">See also</span></span>



[<span data-ttu-id="422e5-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="422e5-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="422e5-148">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="422e5-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="422e5-149">PidTagTemplateid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="422e5-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="422e5-150">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="422e5-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

