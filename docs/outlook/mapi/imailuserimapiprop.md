---
title: imailuser imapiprop
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
# <a name="imailuser--imapiprop"></a><span data-ttu-id="69417-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="69417-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="69417-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69417-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69417-105">メッセージングユーザーに関連付けられている多くのプロパティへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="69417-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="69417-106">**imailuser**インターフェイスは、メッセージングユーザーオブジェクトによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="69417-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="69417-107">**imailuser**は、 [imapiprop: IUnknown](imapipropiunknown.md)インターフェイスから継承し、独自の独自のメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="69417-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69417-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="69417-108">Header file:</span></span>  <br/> |<span data-ttu-id="69417-109">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69417-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="69417-110">公開者:</span><span class="sxs-lookup"><span data-stu-id="69417-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="69417-111">メッセージングユーザーオブジェクト</span><span class="sxs-lookup"><span data-stu-id="69417-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="69417-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="69417-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="69417-113">アドレス帳プロバイダー</span><span class="sxs-lookup"><span data-stu-id="69417-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="69417-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="69417-114">Called by:</span></span>  <br/> |<span data-ttu-id="69417-115">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="69417-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="69417-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="69417-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="69417-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="69417-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="69417-118">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="69417-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="69417-119">lpmailuser</span><span class="sxs-lookup"><span data-stu-id="69417-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="69417-120">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="69417-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="69417-121">一括</span><span class="sxs-lookup"><span data-stu-id="69417-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="69417-122">v の順序</span><span class="sxs-lookup"><span data-stu-id="69417-122">Vtable order</span></span>

<span data-ttu-id="69417-123">このインターフェイスには一意のメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="69417-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="69417-124">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="69417-124">**Required properties**</span></span>|<span data-ttu-id="69417-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="69417-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69417-126">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="69417-127">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="69417-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="69417-128">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="69417-129">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="69417-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="69417-130">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="69417-131">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="69417-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="69417-132">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="69417-133">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="69417-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="69417-134">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="69417-135">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="69417-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="69417-136">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="69417-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="69417-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="69417-138">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="69417-139">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="69417-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="69417-140">**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="69417-141">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="69417-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69417-142">注釈</span><span class="sxs-lookup"><span data-stu-id="69417-142">Remarks</span></span>

<span data-ttu-id="69417-143">必要なプロパティの5つは、受信者のベースアドレスプロパティと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="69417-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="69417-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="69417-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="69417-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="69417-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="69417-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="69417-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="69417-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="69417-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="69417-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="69417-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="69417-149">これらのプロパティは、類似したプロパティの他の多くのグループがこの基本グループに基づいて構築されるため、特別なものと見なされます。</span><span class="sxs-lookup"><span data-stu-id="69417-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="69417-150">他のグループは、メッセージの元の送信者や代理人の送信者など、さまざまな役割で受信者を表すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="69417-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="69417-151">これらのプロパティの詳細と使用方法については、「 [MAPI アドレスの種類](mapi-address-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69417-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="69417-152">メッセージングユーザーは、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティをサポートすることによって、それらのプロパティのコレクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="69417-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="69417-153">**PR_DETAILS_TABLE**は、[詳細] ダイアログボックスのレイアウト、または受信者プロパティ情報を表示するタブ付きプロパティページを説明する表示テーブルです。</span><span class="sxs-lookup"><span data-stu-id="69417-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="69417-154">MAPI は、クライアントが[IAddrBook::D etails](iaddrbook-details.md)メソッドを呼び出すときに、詳細ダイアログボックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="69417-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="69417-155">メッセージングユーザーオブジェクトには、その他のオプションプロパティを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="69417-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="69417-156">MAPI は、メッセージングユーザーに関する追加のアドレス指定情報を提供する多くのプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="69417-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="69417-157">これらのプロパティはすべて文字列です。</span><span class="sxs-lookup"><span data-stu-id="69417-157">All of these properties are character strings.</span></span> <span data-ttu-id="69417-158">次のリストは、よく使用されるプロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="69417-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="69417-159">**PR_ACCOUNT**([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="69417-160">**PR_ASSISTANT**([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="69417-161">**PR_BUSINESS_TELEPHONE_NUMBER**([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="69417-162">**PR_GIVEN_NAME**([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="69417-163">**PR_GOVERNMENT_ID_NUMBER**([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="69417-164">**PR_LOCALITY**([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="69417-165">**PR_POSTAL_ADDRESS**([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69417-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="69417-166">プロパティの完全な一覧については、「[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69417-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="69417-167">関連項目</span><span class="sxs-lookup"><span data-stu-id="69417-167">See also</span></span>



[<span data-ttu-id="69417-168">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="69417-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

