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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c70d16d294426d30f3ac5f00b6bc46992386a86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800447"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="9ba9b-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9ba9b-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="9ba9b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ba9b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ba9b-105">メッセージング ユーザーに関連付けられている多くのプロパティへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="9ba9b-106">**IMailUser**インターフェイスは、メッセージング ユーザーのオブジェクトによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="9ba9b-107">**IMailUser**を継承、 [IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースし、独自の一意のメソッドがありません。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ba9b-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9ba9b-108">Header file:</span></span>  <br/> |<span data-ttu-id="9ba9b-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ba9b-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9ba9b-110">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="9ba9b-111">メッセージングのユーザー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="9ba9b-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="9ba9b-112">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="9ba9b-113">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="9ba9b-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="9ba9b-114">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-114">Called by:</span></span>  <br/> |<span data-ttu-id="9ba9b-115">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="9ba9b-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="9ba9b-116">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9ba9b-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="9ba9b-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="9ba9b-118">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="9ba9b-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="9ba9b-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="9ba9b-120">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="9ba9b-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="9ba9b-121">トランザクション処理</span><span class="sxs-lookup"><span data-stu-id="9ba9b-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9ba9b-122">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="9ba9b-122">Vtable order</span></span>

<span data-ttu-id="9ba9b-123">このインターフェイスには、固有のメソッドがありません。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="9ba9b-124">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-124">**Required properties**</span></span>|<span data-ttu-id="9ba9b-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ba9b-126">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9ba9b-127">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="9ba9b-128">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9ba9b-129">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="9ba9b-130">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9ba9b-131">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ba9b-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="9ba9b-132">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9ba9b-133">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="9ba9b-134">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9ba9b-135">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ba9b-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="9ba9b-136">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9ba9b-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ba9b-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="9ba9b-138">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9ba9b-139">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ba9b-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="9ba9b-140">**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9ba9b-141">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ba9b-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ba9b-142">注釈</span><span class="sxs-lookup"><span data-stu-id="9ba9b-142">Remarks</span></span>

<span data-ttu-id="9ba9b-143">受信者のベース アドレス プロパティとして 5 つの必須プロパティの確認されています。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="9ba9b-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="9ba9b-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="9ba9b-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="9ba9b-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="9ba9b-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="9ba9b-149">これらのプロパティは他の多くのようなプロパティのグループは、この基本のグループに基づいて構築するため、特別なと見なされます。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="9ba9b-150">他のグループのさまざまな役割は、受信者を記述するなど、メッセージの元または送信者に委任されます。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="9ba9b-151">これらのプロパティとその使用方法に関する詳細については、 [MAPI のアドレスの種類](mapi-address-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="9ba9b-152">メッセージング ユーザーは**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティをサポートすることにより、それらのプロパティのコレクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="9ba9b-153">**PR_DETAILS_TABLE**は、[詳細] ダイアログ ボックスまたは受信者のプロパティ情報を表示するタブ付きプロパティ ページのレイアウトを記述するディスプレイ テーブルです。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="9ba9b-154">MAPI では、クライアントは、 [IAddrBook::Details](iaddrbook-details.md)メソッドを呼び出すと、詳細情報がダイアログ ボックスに作成されます。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="9ba9b-155">ユーザー オブジェクトをメッセージに関連するその他のオプションのプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="9ba9b-156">MAPI は、メッセージングのユーザーに関するその他のアドレス情報を提供する多くのプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="9ba9b-157">すべてのこれらのプロパティは、文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-157">All of these properties are character strings.</span></span> <span data-ttu-id="9ba9b-158">一般的に使用されるプロパティを次に示します。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="9ba9b-159">**PR_ACCOUNT**([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9ba9b-160">**PR_ASSISTANT**([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9ba9b-161">**PR_BUSINESS_TELEPHONE_NUMBER**([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9ba9b-162">**PR_GIVEN_NAME**([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9ba9b-163">**PR_GOVERNMENT_ID_NUMBER**([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9ba9b-164">**PR_LOCALITY**([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="9ba9b-165">**PR_POSTAL_ADDRESS**([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ba9b-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="9ba9b-166">プロパティの一覧については、 [MAPI の名前を標準のプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ba9b-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ba9b-167">See also</span></span>



[<span data-ttu-id="9ba9b-168">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9ba9b-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

