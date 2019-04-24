---
title: IProfSect imapiprop
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344794"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="f229e-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f229e-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="f229e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f229e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f229e-105">プロファイルセクションオブジェクトのプロパティと共に動作します。</span><span class="sxs-lookup"><span data-stu-id="f229e-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f229e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f229e-106">Header file:</span></span>  <br/> |<span data-ttu-id="f229e-107">mapix</span><span class="sxs-lookup"><span data-stu-id="f229e-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="f229e-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="f229e-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="f229e-109">Profile section オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f229e-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="f229e-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="f229e-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="f229e-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="f229e-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="f229e-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="f229e-112">Called by:</span></span>  <br/> |<span data-ttu-id="f229e-113">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="f229e-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="f229e-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="f229e-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f229e-115">IID_IProfSect</span><span class="sxs-lookup"><span data-stu-id="f229e-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="f229e-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="f229e-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="f229e-117">LPPROFSECT</span><span class="sxs-lookup"><span data-stu-id="f229e-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="f229e-118">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="f229e-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="f229e-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="f229e-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f229e-120">v の順序</span><span class="sxs-lookup"><span data-stu-id="f229e-120">Vtable order</span></span>

<span data-ttu-id="f229e-121">このインターフェイスには一意のメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="f229e-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="f229e-122">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="f229e-122">**Required properties**</span></span>|<span data-ttu-id="f229e-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="f229e-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f229e-124">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f229e-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f229e-125">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="f229e-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="f229e-126">**PR_PROFILE_NAME**([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f229e-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f229e-127">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="f229e-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="f229e-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f229e-128">Notes to callers</span></span>

<span data-ttu-id="f229e-129">**IProfSect**インターフェイスに独自の固有のメソッドはありませんが、プロファイルセクションの[imapiprop](imapipropiunknown.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="f229e-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="f229e-130">**IProfSect**の実装と**imapiprop**の他の実装には、いくつかの相違点があります。</span><span class="sxs-lookup"><span data-stu-id="f229e-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="f229e-131">**IProfSect**では、トランザクションモデルはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f229e-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="f229e-132">**IProfSect**は、名前付きプロパティをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="f229e-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="f229e-133">**IProfSect**は、セキュリティで保護されたプロパティに対して、identifier range 0x67f0 を0x67f0 に予約します。</span><span class="sxs-lookup"><span data-stu-id="f229e-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="f229e-134">トランザクションモデルをサポートしていないということは、 [imapiprop:: copyprops](imapiprop-copyprops.md)および[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドへの呼び出しの後、プロファイルセクションに加えられたすべての変更が直ちに実行されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="f229e-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="f229e-135">[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドの呼び出しは成功しますが、変更は実際には保存されません。</span><span class="sxs-lookup"><span data-stu-id="f229e-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="f229e-136">途中で発生した変更から保護するために、サービスプロバイダーは、プロパティシートを通じてユーザーに表示されるプロファイルセクションのコピーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f229e-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="f229e-137">プロパティシートは、実際のプロファイルセクションではなく、コピーで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f229e-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="f229e-138">ユーザーが **[OK** ] ボタンをクリックして変更が正確であることを確認すると、変更内容を [実際のプロファイル] セクションに保存することができます。</span><span class="sxs-lookup"><span data-stu-id="f229e-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="f229e-139">[コピーされたプロファイル] セクションを使用してプロパティシートを実装するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="f229e-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="f229e-140">[imapisupport:: openプロファイル](imapisupport-openprofilesection.md)のセクションまたは[IProviderAdmin:: openprofile](iprovideradmin-openprofilesection.md)の開始方法を呼び出すことによって、プロファイルセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="f229e-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="f229e-141">[createiprop](createiprop.md)関数を呼び出して、プロパティデータオブジェクト ( **ipropdata**インターフェイスをサポートするオブジェクト) を取得します。</span><span class="sxs-lookup"><span data-stu-id="f229e-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="f229e-142">プロファイルセクションの[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドを呼び出して、プロパティシートに表示されるプロパティをプロファイルセクションからプロパティデータオブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f229e-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="f229e-143">[imapisupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md)メソッドを呼び出して、サービスプロバイダーにプロパティシートが表示されるように要求し、 _lpconfigdata_パラメーターのプロパティデータオブジェクトへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="f229e-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="f229e-144">ユーザーがプロパティシートの構成プロパティに加えた変更を保存するときには、 [imapiprop:: CopyTo](imapiprop-copyto.md)メソッドを呼び出して、プロパティデータオブジェクトからプロファイルセクションにプロパティをコピーして戻します。</span><span class="sxs-lookup"><span data-stu-id="f229e-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="f229e-145">プロファイルセクションは、他のオブジェクトとは異なり、名前付きプロパティをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="f229e-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="f229e-146">[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)および[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドは、プロファイルセクションオブジェクトで呼び出された場合、MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="f229e-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="f229e-147">[imapiprop:: setprops](imapiprop-setprops.md)メソッドを使用して、0x8000 を超える範囲のプロパティ識別子を設定すると、PT_ERROR プロパティの型が返されます。</span><span class="sxs-lookup"><span data-stu-id="f229e-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="f229e-148">プロファイルセクションでは、セキュリティで保護されたプロパティに対して識別子範囲0x67f0 から0x67f0 を予約します。</span><span class="sxs-lookup"><span data-stu-id="f229e-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="f229e-149">サービスプロバイダーは、この範囲を使用して、パスワードやその他のプロバイダー固有の資格情報を格納できます。</span><span class="sxs-lookup"><span data-stu-id="f229e-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="f229e-150">この範囲内のプロパティは、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドの_lpPropTag_パラメーターで NULL が渡されたときに、プロパティの完全な一覧に返されません。 __ または、 [imapiprop:: getproplist](imapiprop-getproplist.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="f229e-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="f229e-151">セキュリティで保護されたプロパティは、識別子によって明示的に要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f229e-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="f229e-152">MAPI furnishes は、ハードコードされた定数 MUID_PROFILE_INSTANCE を持つプロファイルセクションを識別子として、 **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) を1つのプロパティとして使用します。</span><span class="sxs-lookup"><span data-stu-id="f229e-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="f229e-153">MAPI を使用すると、作成されたすべてのプロファイルで**PR_SEARCH_KEY**プロパティの値が一意になることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="f229e-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="f229e-154">一意性が重要な場合は、 **PR_PROFILE_NAME**の代わりに**PR_SEARCH_KEY**を使用します。これは、削除されたプロファイルの後に同じ名前の別のプロファイルが続く可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="f229e-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="f229e-155">プロファイルセクションの使用方法の詳細については、「[プロファイルおよびメッセージサービスを管理](administering-profiles-and-message-services.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f229e-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f229e-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="f229e-156">See also</span></span>



[<span data-ttu-id="f229e-157">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="f229e-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

