---
title: 受信者の準備
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b4ccfb8cf8201a17993932acc4c0104ace80b94d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588721"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="99530-103">受信者の準備</span><span class="sxs-lookup"><span data-stu-id="99530-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="99530-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99530-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99530-105">クライアント アプリケーションでは、長期のエントリ id を短期的なエントリの識別子を変換して可能性のある追加、変更、またはプロパティの順序を変更して受信者を準備します。</span><span class="sxs-lookup"><span data-stu-id="99530-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="99530-106">メッセージの受信者のリストの一部である受信者またはメッセージに関連ではない受信者を準備できます。</span><span class="sxs-lookup"><span data-stu-id="99530-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="99530-107">通常、クライアントは、共通のアドレス] ダイアログ ボックスに含まれる受信者のエントリ id を長期的な短期的なエントリの識別子に変換するには、直接[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="99530-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="99530-108">送信メッセージに関連付けられている受信者、受信者の準備が名前解決処理によって処理されます。</span><span class="sxs-lookup"><span data-stu-id="99530-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="99530-109">受信者の一覧を作成するには、 **IAddrBook::PrepareRecips**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="99530-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="99530-110">**PrepareRecips**は、 [ADRLIST](adrlist.md)構造体とプロパティ タグのリストを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="99530-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="99530-111">**ADRLIST**構造体には、タグのプロパティ] ボックスの一覧は、各受信者をサポートする必要がありますプロパティを表すときに準備を整えるための受信者が含まれています。</span><span class="sxs-lookup"><span data-stu-id="99530-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="99530-112">**PrepareRecips**は、 **ADRLIST**構造体の先頭のプロパティ タグのリストに含まれているプロパティを配置しようとします。</span><span class="sxs-lookup"><span data-stu-id="99530-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="99530-113">**ADRLIST**構造体から、リスト内のプロパティのいずれかが表示されない、MAPI は、それらを提供するアドレス帳プロバイダーを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="99530-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="99530-114">長期のエントリ id を確認する必要がある場合は、 _lpSPropTagArray_パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="99530-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="99530-115">たとえば、5 人の受信者を使用するいるとします。</span><span class="sxs-lookup"><span data-stu-id="99530-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="99530-116">5 つのすべての受信者が、 **ADRLIST**構造体に次の順序で次のプロパティに表示されます。</span><span class="sxs-lookup"><span data-stu-id="99530-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="99530-117">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99530-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="99530-118">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99530-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="99530-119">**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99530-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="99530-120">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99530-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="99530-121">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99530-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="99530-122">他の 3 つのプロパティは、最初の 2 つの受信者の**ADRLIST**構造体に含まれます。</span><span class="sxs-lookup"><span data-stu-id="99530-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="99530-123">**PR_ACCOUNT**([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99530-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="99530-124">**PR_GIVEN_NAME**([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99530-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="99530-125">**PR_SURNAME**([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99530-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="99530-126">**PR_ADDRTYPE**、 **PR_ENTRYID**、および**PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)) の最初の 3 つのプロパティとして持つすべての受信者のため、これらのプロパティを持つプロパティ タグ配列を作成し、渡す**PrepareRecips**、 **ADRLIST**構造体です。</span><span class="sxs-lookup"><span data-stu-id="99530-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="99530-127">**PrepareRecips**は現在、 **ADRLIST**構造体の一部ではないので、 **PR_HOME_TELEPHONE_NUMBER**を取得するために、各受信者の**IMAPIProp::GetProps**メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="99530-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="99530-128">**PrepareRecips**が返されると、受信者の一覧は、受信者ごとに最初に表示する**ADRLIST**構造体に含まれているプロパティを使用して差し込み印刷の受信者の一覧を表します。</span><span class="sxs-lookup"><span data-stu-id="99530-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="99530-129">1 と 2 の宛先の受信者の一覧には、次の順序でプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="99530-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="99530-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="99530-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="99530-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="99530-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="99530-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="99530-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="99530-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="99530-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="99530-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="99530-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="99530-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="99530-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="99530-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="99530-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="99530-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="99530-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="99530-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="99530-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="99530-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="99530-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="99530-140">3、4、および 5 の宛先の受信者の一覧には、次の順序でプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="99530-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="99530-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="99530-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="99530-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="99530-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="99530-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="99530-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="99530-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="99530-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="99530-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="99530-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="99530-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="99530-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="99530-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="99530-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="99530-148">プロパティを操作する**IAddrBook::PrepareRecips**を呼び出す代わりに、各受信者の[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すと、必要であれば、その[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="99530-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="99530-149">のみ 1 人の受信者が関係する場合は、いずれかの技法は、満足のいく。</span><span class="sxs-lookup"><span data-stu-id="99530-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="99530-150">ただし、複数の受信者が含まれる場合は、時間の節約**IMAPIProp**メソッドではなく、 **PrepareRecips**を呼び出すと、している場合、リモートで多くのリモート プロシージャ コールします。</span><span class="sxs-lookup"><span data-stu-id="99530-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="99530-151">**GetProps**と**SetProps**は、受信者ごとに 1 つの呼び出しを行う一方、 **PrepareRecips**は 1 回の呼び出しのすべての受信者を処理します。</span><span class="sxs-lookup"><span data-stu-id="99530-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

