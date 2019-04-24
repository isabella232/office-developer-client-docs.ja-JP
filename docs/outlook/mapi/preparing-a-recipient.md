---
title: 受信者の準備
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350674"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="1c9e0-103">受信者の準備</span><span class="sxs-lookup"><span data-stu-id="1c9e0-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="1c9e0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c9e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c9e0-105">クライアントアプリケーションは、短い用語のエントリ識別子を長期のエントリ識別子に変換して、プロパティの追加、変更、または並べ替えを行うことにより、受信者を事前に準備します。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="1c9e0-106">メッセージに関連付けられていない受信者リストの一部である受信者を準備することができます。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="1c9e0-107">通常、クライアントは[IAddrBook::P reparerecips](iaddrbook-preparerecips.md)を呼び出して、短い用語の入力識別子を、[共通アドレス] ダイアログボックスに含まれている受信者の長期エントリ識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="1c9e0-108">送信メッセージに関連付けられている受信者の場合、受信者の準備は名前解決プロセスによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="1c9e0-109">受信者の一覧を準備するには、 **IAddrBook::P reparerecips**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="1c9e0-110">**PrepareRecips**は、 [adrlist](adrlist.md)構造とプロパティタグのリストを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="1c9e0-111">**adrlist**構造体には、各受信者がサポートするプロパティをプロパティタグリストが表す間に準備する受信者が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="1c9e0-112">**PrepareRecips**は、 **adrlist**構造の先頭に、プロパティタグリストに含まれるプロパティを配置しようとします。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="1c9e0-113">リスト内のプロパティのいずれかが**adrlist**構造に欠落している場合、MAPI はアドレス帳プロバイダーを呼び出して指定します。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="1c9e0-114">長期のエントリ識別子のみをチェックする必要がある場合は、 _lpSPropTagArray_パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="1c9e0-115">たとえば、5人の受信者で作業しているとします。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="1c9e0-116">すべての5人の受信者は、次の順序で、以下のプロパティを持つ**adrlist**構造に表示されます。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="1c9e0-117">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c9e0-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="1c9e0-118">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c9e0-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="1c9e0-119">**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c9e0-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="1c9e0-120">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c9e0-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="1c9e0-121">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c9e0-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="1c9e0-122">最初の2つの受信者の**adrlist**構造には、他に3つのプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="1c9e0-123">**PR_ACCOUNT**([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c9e0-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="1c9e0-124">**PR_GIVEN_NAME**([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c9e0-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="1c9e0-125">**PR_SURNAME**([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c9e0-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="1c9e0-126">すべての受信者が最初の3つのプロパティ**PR_ADDRTYPE**、 **PR_ENTRYID**、および**PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)) を必要とするため、これらのプロパティを使用してプロパティタグ配列を作成し、渡します。**PrepareRecips**には、これと**adrlist**構造があります。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="1c9e0-127">**PrepareRecips**は、現在**adrlist**構造体の一部ではないため、各受信者の**imapiprop:: GetProps**メソッドを呼び出して、 **PR_HOME_TELEPHONE_NUMBER**を取得します。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="1c9e0-128">**PrepareRecips**が戻ると、受信者リストは、各受信者に対して最初に表示される**adrlist**構造に含まれるプロパティを持つ受信者の結合されたリストを表します。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="1c9e0-129">受信者1および2の受信者の一覧には、次の順序でプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="1c9e0-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="1c9e0-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="1c9e0-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="1c9e0-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="1c9e0-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="1c9e0-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="1c9e0-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="1c9e0-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="1c9e0-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="1c9e0-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="1c9e0-140">受信者3、4、および5の受信者の一覧には、次の順序でプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="1c9e0-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="1c9e0-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="1c9e0-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="1c9e0-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="1c9e0-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="1c9e0-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="1c9e0-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="1c9e0-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="1c9e0-148">**IAddrBook::P reparerecips**を呼び出してプロパティを処理する代わりに、各受信者の[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出し、必要に応じて[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="1c9e0-149">参加する受信者が1人だけの場合は、どちらの方法でも十分です。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="1c9e0-150">ただし、複数の受信者が関係している場合は、 **imapiprop**メソッドではなく**PrepareRecips**を呼び出すと時間が節約され、リモートで操作している場合はリモートプロシージャコールの数が多くなります。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="1c9e0-151">**PrepareRecips**は、すべての受信者を1回の呼び出しで処理し、 **GetProps**と**setprops**は各受信者に対して1つの呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="1c9e0-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

