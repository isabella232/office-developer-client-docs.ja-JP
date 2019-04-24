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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326363"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="4f9f6-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="4f9f6-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="4f9f6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f9f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f9f6-105">外部アドレス帳プロバイダーの受信者エントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="4f9f6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4f9f6-106">Parameters</span></span>

 <span data-ttu-id="4f9f6-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="4f9f6-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="4f9f6-108">順番_lpTemplateID_によって示されるテンプレート識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="4f9f6-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="4f9f6-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="4f9f6-110">順番開く受信者エントリのテンプレート識別子**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="4f9f6-111">_ultemplateflags_</span><span class="sxs-lookup"><span data-stu-id="4f9f6-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="4f9f6-112">順番エントリを開く方法を示すために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="4f9f6-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-113">The following flag can be set:</span></span>
    
<span data-ttu-id="4f9f6-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="4f9f6-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="4f9f6-115">新しいエントリが作成されています。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-115">A new entry is being created.</span></span> <span data-ttu-id="4f9f6-116">外部プロバイダーは、MAPI から[IABLogon:: OpenTemplateID](iablogon-opentemplateid.md)呼び出しを受け取ると、 _lpMAPIPropData_パラメーターで指定されたプロパティを変更するか、特定のインターフェイスを返すことにより、エントリの作成方法を制御できます。_lppMAPIPropNew_での実装。新しいエントリのプロパティを設定する方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="4f9f6-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="4f9f6-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="4f9f6-118">順番発信者がエントリにアクセスするために使用するインターフェイスの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="4f9f6-119">これは、外部プロバイダーが独自の実装でラップして、 _lppMAPIPropNew_パラメーターで返す実装です。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="4f9f6-120">_lpMAPIPropData_パラメーターは、 [imapiprop: IUnknown](imapipropiunknown.md)から派生した読み取り/書き込みインターフェイスの実装を指している必要があり、 _lpinterface_パラメーターで要求されているインターフェイスをサポートしていなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="4f9f6-121">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="4f9f6-121">_lpInterface_</span></span>
  
> <span data-ttu-id="4f9f6-122">順番エントリへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="4f9f6-123">_lppMAPIPropNew_パラメーターは、 _lpinterface_で指定された型のインターフェイスを指します。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="4f9f6-124">NULL を渡すと、メッセージングユーザー IID_IMailUser の標準インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="4f9f6-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="4f9f6-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="4f9f6-126">読み上げ外部プロバイダーがエントリにアクセスするために提供するインターフェイスの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="4f9f6-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="4f9f6-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="4f9f6-128">予約語NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f9f6-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="4f9f6-129">Return value</span></span>

<span data-ttu-id="4f9f6-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f9f6-130">S_OK</span></span> 
  
> <span data-ttu-id="4f9f6-131">バインドプロセスが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-131">The binding process was successful.</span></span>
    
<span data-ttu-id="4f9f6-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4f9f6-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="4f9f6-133">外部アドレス帳プロバイダーが存在しません。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f9f6-134">解説</span><span class="sxs-lookup"><span data-stu-id="4f9f6-134">Remarks</span></span>

<span data-ttu-id="4f9f6-135">**imapisupport:: OpenTemplateID**メソッドは、アドレス帳プロバイダーサポートオブジェクトに対してのみ実装されています。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="4f9f6-136">**OpenTemplateID**は、他のアドレス帳プロバイダー (外部プロバイダーとも呼ばれる) に属するエントリに対してホストとして動作するアドレス帳プロバイダーによってのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="4f9f6-137">ホストプロバイダーは、 **OpenTemplateID**を呼び出して外部エントリを開きます。これは、ホストプロバイダーのデータが外部プロバイダーのコードにバインドされるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4f9f6-138">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4f9f6-138">Notes to callers</span></span>

<span data-ttu-id="4f9f6-139">**OpenTemplateID**の呼び出しは、外部アドレス帳プロバイダーからのテンプレート識別子を持つエントリの格納をサポートしている場合にのみ行います。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="4f9f6-140">このようなサポートでは、 [IABContainer:: createentry](iabcontainer-createentry.md)および[IABLogon:: openentry](iablogon-openentry.md)実装に追加の要件があります。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="4f9f6-141">詳細については、これらのメソッドの説明を参照し、[ホストアドレス帳プロバイダーとして機能](acting-as-a-host-address-book-provider.md)します。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="4f9f6-142">**OpenTemplateID**呼び出しが、渡されたのと同じ property オブジェクトの実装で、バインドされたインターフェイスとして返される場合は、property オブジェクトへの参照を解放することができます。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="4f9f6-143">これは、外部プロバイダーがオブジェクトの**AddRef**メソッドを呼び出して、独自の参照を保持しているためです。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="4f9f6-144">外部プロバイダーが property オブジェクトへの参照を保持する必要がない場合、 **OpenTemplateID**は、非連結プロパティオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="4f9f6-145">**OpenTemplateID**が MAPI_E_UNKNOWN_ENTRYID で失敗する場合は、エントリを読み取り専用として処理することによって続行します。</span><span class="sxs-lookup"><span data-stu-id="4f9f6-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f9f6-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f9f6-146">See also</span></span>



[<span data-ttu-id="4f9f6-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="4f9f6-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="4f9f6-148">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4f9f6-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="4f9f6-149">PidTagTemplateid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f9f6-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="4f9f6-150">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f9f6-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

