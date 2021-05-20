---
title: IMailUser IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436595"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="de8bf-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="de8bf-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="de8bf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de8bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de8bf-105">メッセージング ユーザーに関連付けられている多くのプロパティへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="de8bf-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="de8bf-106">**IMailUser インターフェイスは**、メッセージング ユーザー オブジェクトによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="de8bf-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="de8bf-107">**IMailUser は** [IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスから継承され、独自の固有のメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="de8bf-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de8bf-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="de8bf-108">Header file:</span></span>  <br/> |<span data-ttu-id="de8bf-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de8bf-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="de8bf-110">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="de8bf-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="de8bf-111">メッセージング ユーザー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="de8bf-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="de8bf-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="de8bf-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="de8bf-113">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="de8bf-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="de8bf-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="de8bf-114">Called by:</span></span>  <br/> |<span data-ttu-id="de8bf-115">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="de8bf-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="de8bf-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="de8bf-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="de8bf-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="de8bf-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="de8bf-118">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="de8bf-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="de8bf-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="de8bf-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="de8bf-120">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="de8bf-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="de8bf-121">Transacted</span><span class="sxs-lookup"><span data-stu-id="de8bf-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="de8bf-122">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="de8bf-122">Vtable order</span></span>

<span data-ttu-id="de8bf-123">このインターフェイスには、一意のメソッドが含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="de8bf-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="de8bf-124">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="de8bf-124">**Required properties**</span></span>|<span data-ttu-id="de8bf-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="de8bf-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de8bf-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="de8bf-127">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="de8bf-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="de8bf-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="de8bf-129">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="de8bf-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="de8bf-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="de8bf-131">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="de8bf-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="de8bf-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="de8bf-133">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="de8bf-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="de8bf-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="de8bf-135">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="de8bf-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="de8bf-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="de8bf-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="de8bf-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="de8bf-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="de8bf-139">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="de8bf-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="de8bf-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="de8bf-141">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="de8bf-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de8bf-142">注釈</span><span class="sxs-lookup"><span data-stu-id="de8bf-142">Remarks</span></span>

<span data-ttu-id="de8bf-143">必要なプロパティの 5 つを、受信者の基本アドレス プロパティと呼ばれる。</span><span class="sxs-lookup"><span data-stu-id="de8bf-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="de8bf-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="de8bf-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="de8bf-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="de8bf-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="de8bf-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="de8bf-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="de8bf-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="de8bf-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="de8bf-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="de8bf-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="de8bf-149">これらのプロパティは、この基本グループの上に類似するプロパティの他の多くのグループが構築されているので、特別と見なされます。</span><span class="sxs-lookup"><span data-stu-id="de8bf-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="de8bf-150">他のグループは、メッセージの元の送信者や代理人の送信者など、さまざまな役割の受信者を記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de8bf-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="de8bf-151">これらのプロパティとそれらを使用する方法の詳細については、「MAPI アドレスの種類 [」を参照してください](mapi-address-types.md)。</span><span class="sxs-lookup"><span data-stu-id="de8bf-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="de8bf-152">メッセージング ユーザーは、プロパティ ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md) **)** プロパティをサポートPR_DETAILS_TABLEプロパティのコレクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="de8bf-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="de8bf-153">**PR_DETAILS_TABLE** は、詳細ダイアログ ボックスのレイアウト、または受信者のプロパティ情報を表示するタブ付きプロパティ ページを示す表示テーブルです。</span><span class="sxs-lookup"><span data-stu-id="de8bf-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="de8bf-154">MAPI は、クライアントが [IAddrBook::Dメソッドを呼び出:Dダイアログ ボックスを作成](iaddrbook-details.md) します。</span><span class="sxs-lookup"><span data-stu-id="de8bf-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="de8bf-155">メッセージング ユーザー オブジェクトには、他の省略可能なプロパティを関連付けできます。</span><span class="sxs-lookup"><span data-stu-id="de8bf-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="de8bf-156">MAPI は、メッセージング ユーザーに関する追加のアドレス情報を提供する多くのプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="de8bf-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="de8bf-157">これらのプロパティはすべて文字列です。</span><span class="sxs-lookup"><span data-stu-id="de8bf-157">All of these properties are character strings.</span></span> <span data-ttu-id="de8bf-158">次の一覧は、より一般的に使用されるプロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="de8bf-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="de8bf-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="de8bf-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="de8bf-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="de8bf-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="de8bf-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="de8bf-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="de8bf-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de8bf-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="de8bf-166">プロパティの完全な一覧については [、「Mapping Canonical Property Names to MAPI Names」を参照してください](mapping-canonical-property-names-to-mapi-names.md)。</span><span class="sxs-lookup"><span data-stu-id="de8bf-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="de8bf-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="de8bf-167">See also</span></span>



[<span data-ttu-id="de8bf-168">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="de8bf-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

