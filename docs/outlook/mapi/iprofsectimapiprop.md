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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406599"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="2a6b4-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2a6b4-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="2a6b4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a6b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a6b4-105">プロファイル セクション オブジェクトのプロパティを操作します。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a6b4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2a6b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="2a6b4-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="2a6b4-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="2a6b4-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="2a6b4-109">プロファイル セクション オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2a6b4-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="2a6b4-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="2a6b4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="2a6b4-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="2a6b4-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="2a6b4-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="2a6b4-112">Called by:</span></span>  <br/> |<span data-ttu-id="2a6b4-113">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="2a6b4-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="2a6b4-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="2a6b4-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2a6b4-115">IID_IProfSect</span><span class="sxs-lookup"><span data-stu-id="2a6b4-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="2a6b4-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="2a6b4-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="2a6b4-117">LPPROFSECT</span><span class="sxs-lookup"><span data-stu-id="2a6b4-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="2a6b4-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="2a6b4-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="2a6b4-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="2a6b4-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2a6b4-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="2a6b4-120">Vtable order</span></span>

<span data-ttu-id="2a6b4-121">このインターフェイスには、一意のメソッドが含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="2a6b4-122">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="2a6b4-122">**Required properties**</span></span>|<span data-ttu-id="2a6b4-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="2a6b4-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a6b4-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2a6b4-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2a6b4-125">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="2a6b4-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="2a6b4-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2a6b4-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2a6b4-127">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="2a6b4-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="2a6b4-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2a6b4-128">Notes to callers</span></span>

<span data-ttu-id="2a6b4-129">**IProfSect** インターフェイスには独自の一意のメソッドは存在しないが、プロファイル セクションの [IMAPIProp](imapipropiunknown.md)メソッドを呼び出す事が可能です。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="2a6b4-130">**IProfSect** 実装と IMAPIProp の他の実装にはいくつかの違 **いがあります**。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="2a6b4-131">**IProfSect は** トランザクション モデルをサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="2a6b4-132">**IProfSect では** 、名前付きプロパティはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="2a6b4-133">**IProfSect は** 、セキュリティで保護されたプロパティ0x67F0に0x67ff識別子の範囲を予約します。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="2a6b4-134">トランザクション モデルをサポートしていない場合は [、IMAPIProp::CopyProps](imapiprop-copyprops.md) メソッドと [IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドの呼び出し後にプロファイル セクションに加えたすべての変更が直ちに行われます。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="2a6b4-135">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの呼び出しは成功しますが、実際には変更は保存しません。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="2a6b4-136">途中で発生する変更から保護するには、サービス プロバイダーは、プロパティ シートを使用してユーザーに表示されるプロファイル セクションのコピーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="2a6b4-137">プロパティ シートは、実際のプロファイル セクションではなく、コピーで動作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="2a6b4-138">ユーザーが **[OK]** ボタンをクリックして変更が正確に行われたか確認すると、変更を実際のプロファイル セクションに保存できます。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="2a6b4-139">コピーしたプロファイル セクションを使用してプロパティ シートを実装するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="2a6b4-140">[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)または[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md)メソッドを呼び出して、プロファイル セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="2a6b4-141">[CreateIProp 関数を呼](createiprop.md)び出して、プロパティ データ オブジェクト **(IPropData** インターフェイスをサポートするオブジェクト) を取得します。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="2a6b4-142">プロファイル セクションの [IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドを呼び出して、プロパティ シートに表示されるプロパティをプロファイル セクションからプロパティ データ オブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="2a6b4-143">[IMAPISupport::D oConfigPropSheet](imapisupport-doconfigpropsheet.md)メソッドを呼び出して、サービス プロバイダーにプロパティ シートの表示を要求し _、lpConfigData_ パラメーターのプロパティ データ オブジェクトへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="2a6b4-144">ユーザーがプロパティ シートに構成プロパティの変更を保存する場合は [、IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドを呼び出して、プロパティ データ オブジェクトからプロファイル セクションにプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="2a6b4-145">プロファイル セクションは、他のオブジェクトとは異なり、名前付きプロパティをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="2a6b4-146">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)および[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドは、プロファイル セクション オブジェクトで呼び出された場合、MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="2a6b4-147">[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを使用して、0x8000 の上の範囲でプロパティ識別子を設定すると、PT_ERROR プロパティの種類が返されます。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="2a6b4-148">プロファイル セクションでは、セキュリティで保護されたプロパティ0x67F0 0x67FF識別子の範囲を予約します。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="2a6b4-149">サービス プロバイダーは、この範囲を使用して、パスワードや他のプロバイダー固有の資格情報を格納できます。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="2a6b4-150">この範囲のプロパティは [、IMAPIProp::GetProps](imapiprop-getprops.md)メソッドの _lpPropTag_ パラメーターで NULL が渡された場合、プロパティの完全な一覧には返されません。[また、IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドの _lppPropTagArray_ パラメーターでは返されません。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="2a6b4-151">セキュリティで保護されたプロパティは、識別子によって特に要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="2a6b4-152">MAPI は、ハードコードされた定数を持つプロファイル セクションMUID_PROFILE_INSTANCE識別子として、PR_SEARCH_KEY **(** [PidTagSearchKey](pidtagsearchkey-canonical-property.md)) を単一のプロパティとして指定します。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="2a6b4-153">MAPI を使用すると **、PR_SEARCH_KEYプロパティ** の値が作成されたプロファイルの中で一意になります。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="2a6b4-154">一 **PR_SEARCH_KEY** が重要なPR_PROFILE_NAMEの代わりに、削除されたプロファイルの後に同じ名前の別のプロファイルが続く可能性がある場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="2a6b4-155">プロファイル セクションの使用方法の詳細については、「プロファイルとメッセージ サービスの管理 [」を参照してください](administering-profiles-and-message-services.md)。</span><span class="sxs-lookup"><span data-stu-id="2a6b4-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2a6b4-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a6b4-156">See also</span></span>



[<span data-ttu-id="2a6b4-157">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="2a6b4-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

