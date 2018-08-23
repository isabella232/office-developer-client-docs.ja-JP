---
title: IProfSect IMAPIProp
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
ms.openlocfilehash: c0653caec5f3cac531206e1bb9c4330cac5f3133
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801158"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="bc28f-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bc28f-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="bc28f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc28f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc28f-105">プロファイル セクション オブジェクトのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc28f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bc28f-106">Header file:</span></span>  <br/> |<span data-ttu-id="bc28f-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="bc28f-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="bc28f-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="bc28f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="bc28f-109">プロファイル セクションのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="bc28f-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="bc28f-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="bc28f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="bc28f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="bc28f-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="bc28f-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="bc28f-112">Called by:</span></span>  <br/> |<span data-ttu-id="bc28f-113">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="bc28f-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="bc28f-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="bc28f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bc28f-115">IID_IProfSect</span><span class="sxs-lookup"><span data-stu-id="bc28f-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="bc28f-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="bc28f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="bc28f-117">LPPROFSECT</span><span class="sxs-lookup"><span data-stu-id="bc28f-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="bc28f-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="bc28f-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="bc28f-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="bc28f-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bc28f-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="bc28f-120">Vtable order</span></span>

<span data-ttu-id="bc28f-121">このインターフェイスには、固有のメソッドがありません。</span><span class="sxs-lookup"><span data-stu-id="bc28f-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="bc28f-122">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="bc28f-122">**Required properties**</span></span>|<span data-ttu-id="bc28f-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="bc28f-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc28f-124">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc28f-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bc28f-125">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="bc28f-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="bc28f-126">**PR_PROFILE_NAME**([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc28f-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bc28f-127">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="bc28f-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="bc28f-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="bc28f-128">Notes to callers</span></span>

<span data-ttu-id="bc28f-129">**IProfSect**インターフェイスには、独自の固有のメソッドはありませんが、プロファイル セクションの[IMAPIProp](imapipropiunknown.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="bc28f-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="bc28f-130">いくつかの違いは、 **IProfSect**の実装と他の**IMAPIProp**の実装があります。</span><span class="sxs-lookup"><span data-stu-id="bc28f-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="bc28f-131">**IProfSect**は、トランザクション モデルをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="bc28f-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="bc28f-132">**IProfSect**では、名前付きプロパティはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bc28f-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="bc28f-133">**IProfSect**は、セキュリティで保護されたプロパティの識別子の範囲 0x67F0 に 0x67ff を予約します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="bc28f-134">対して行ったすべての変更、プロファイルのセクションで次を呼び出すこと[IMAPIProp::CopyProps](imapiprop-copyprops.md)には、トランザクション モデルをサポートしていないと、 [IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドがすぐに発生します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="bc28f-135">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドへの呼び出しは成功ですが、実際に変更を保存できません。</span><span class="sxs-lookup"><span data-stu-id="bc28f-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="bc28f-136">処理の途中で行われる変更から保護するには、サービス プロバイダーは、プロパティ シートを使用してユーザーに表示される自分のプロファイル セクションのコピーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc28f-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="bc28f-137">プロパティ シートには、実際のプロファイル セクションではなく、コピーが動作します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="bc28f-138">ユーザーは、変更内容が正確であることを確認するのには [ **OK** ] ボタンをクリックすると、ときに、実際のプロファイル セクションに変更を保存できます。</span><span class="sxs-lookup"><span data-stu-id="bc28f-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="bc28f-139">コピー先のプロファイル セクションを使用してプロパティ シートを実装するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="bc28f-140">[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)または[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md)メソッドを呼び出すことによって、[プロファイル] セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="bc28f-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="bc28f-141">プロパティのデータ オブジェクトを取得する[CreateIProp](createiprop.md)関数を呼び出して、 **IPropData**インターフェイスをサポートするオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="bc28f-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="bc28f-142">プロパティのデータ オブジェクトを [プロファイル] セクションのプロパティ シートに表示されるプロパティをコピーするのには、プロファイルのセクションの[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="bc28f-143">サービス プロバイダーは、プロパティ シートを表示および_lpConfigData_パラメーターのプロパティのデータ オブジェクトへのポインターを渡すことを要求する[IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="bc28f-144">プロパティ シートで設定のプロパティに変更を保存すると、ときに、プロパティのデータ オブジェクトから、[プロファイル] セクションにプロパティをコピーするのには[IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="bc28f-145">他のオブジェクトとは異なり、プロファイルのセクションでは、名前付きプロパティをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="bc28f-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="bc28f-146">プロファイル セクションのオブジェクトで呼び出される場合、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドと[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドは MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="bc28f-147">0x8000 以上の範囲のプロパティの識別子を設定するのには、 [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを使用する場合は、PT_ERROR プロパティの型が返されます。</span><span class="sxs-lookup"><span data-stu-id="bc28f-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="bc28f-148">プロファイル セクションでは、セキュリティで保護されたプロパティの識別子の範囲 0x67F0 に 0x67FF を予約します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="bc28f-149">サービス プロバイダーは、パスワードおよびその他のプロバイダーに固有の資格情報を格納するのには、この範囲を使用できます。</span><span class="sxs-lookup"><span data-stu-id="bc28f-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="bc28f-150">[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドの_lpPropTag_パラメーターに NULL が渡されたとき、[の_lppPropTagArray_パラメーターに返される、プロパティの完全なリストでこの範囲内のプロパティは返されませんIMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="bc28f-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="bc28f-151">セキュリティで保護されたプロパティは、それらの識別子を具体的に要求しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="bc28f-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="bc28f-152">MAPI は、1 つのプロパティとして識別子と定数 MUID_PROFILE_INSTANCE をハード コーディングされた**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) とのプロファイル セクションを提供します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="bc28f-153">MAPI は、 **PR_SEARCH_KEY**プロパティの値を作成したすべてのプロファイルの中で一意になることを保証します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="bc28f-154">削除するプロファイルを別のプロファイルと同じ名前の後に可能性があるために、一意性が重要では場合は、 **PR_PROFILE_NAME**ではなく**PR_SEARCH_KEY**を使用します。</span><span class="sxs-lookup"><span data-stu-id="bc28f-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="bc28f-155">プロファイルのセクションを使用する方法の詳細については、 [[プロファイルの管理とメッセージ サービス](administering-profiles-and-message-services.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc28f-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bc28f-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc28f-156">See also</span></span>



[<span data-ttu-id="bc28f-157">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="bc28f-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

