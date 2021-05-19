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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419878"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="685bc-103">受信者の準備</span><span class="sxs-lookup"><span data-stu-id="685bc-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="685bc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="685bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="685bc-105">クライアント アプリケーションは、短期的なエントリ識別子を長期エントリ識別子に変換し、プロパティを追加、変更、または並べ替えることによって受信者を準備します。</span><span class="sxs-lookup"><span data-stu-id="685bc-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="685bc-106">メッセージに関係のないメッセージまたは受信者の受信者リストの一部である受信者を準備できます。</span><span class="sxs-lookup"><span data-stu-id="685bc-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="685bc-107">通常、クライアントは [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) を直接呼び出して、短期エントリ識別子を共通のアドレス ダイアログ ボックスに含まれる受信者の長期エントリ識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="685bc-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="685bc-108">送信メッセージに関連付けられている受信者の場合、受信者の準備は名前解決プロセスによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="685bc-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="685bc-109">受信者のリストを準備するには **、IAddrBook::P repareRecips を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="685bc-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="685bc-110">**PrepareRecips は**[、ADRLIST](adrlist.md)構造とプロパティ タグのリストを受け入れる。</span><span class="sxs-lookup"><span data-stu-id="685bc-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="685bc-111">**ADRLIST 構造には**、準備する受信者が含まれるのに対し、プロパティ タグリストは各受信者がサポートする必要があるプロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="685bc-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="685bc-112">**PrepareRecips は** 、プロパティ タグ リストに含まれるプロパティを **ADRLIST** 構造体の先頭に配置します。</span><span class="sxs-lookup"><span data-stu-id="685bc-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="685bc-113">リスト内のプロパティの 1 つが **ADRLIST** 構造から欠落している場合、MAPI はアドレス帳プロバイダーを呼び出して提供します。</span><span class="sxs-lookup"><span data-stu-id="685bc-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="685bc-114">長期エントリ識別子のみを確認する必要がある場合は  _、lpSPropTagArray_ パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="685bc-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="685bc-115">たとえば、5 人の受信者を操作するとします。</span><span class="sxs-lookup"><span data-stu-id="685bc-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="685bc-116">5 人の受信者すべてが **ADRLIST 構造に表示** され、次のプロパティが次の順序で表示されます。</span><span class="sxs-lookup"><span data-stu-id="685bc-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="685bc-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="685bc-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="685bc-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="685bc-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="685bc-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="685bc-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="685bc-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="685bc-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="685bc-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="685bc-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="685bc-122">最初の 2 つの受信者の **ADRLIST** 構造には、他の 3 つのプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="685bc-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="685bc-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="685bc-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="685bc-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="685bc-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="685bc-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="685bc-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="685bc-126">すべての受信者が最初の **3** つのプロパティ **PR_ADDRTYPE、PR_ENTRYID、** および PR_HOME_TELEPHONE_NUMBER ([PidTagHomeTelephoneNumber)](pidtaghometelephonenumber-canonical-property.md)として持つ必要があるため、これらのプロパティを持つプロパティ タグ配列を作成し、そのプロパティと **ADRLIST** 構造体を **PrepareRecips** に渡します。 </span><span class="sxs-lookup"><span data-stu-id="685bc-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="685bc-127">**PrepareRecips は**、現在 **ADRLIST** 構造の一部ではないので、各受信者の **IMAPIProp::GetProps** メソッドを呼び出して PR_HOME_TELEPHONE_NUMBER を取得します。</span><span class="sxs-lookup"><span data-stu-id="685bc-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="685bc-128">**PrepareRecips が返** される場合、受信者リストは、受信者ごとに最初に表示される **ADRLIST** 構造に含まれるプロパティを持つ、結合された受信者の一覧を表します。</span><span class="sxs-lookup"><span data-stu-id="685bc-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="685bc-129">受信者 1 と受信者 2 の受信者リストには、次の順序でプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="685bc-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="685bc-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="685bc-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="685bc-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="685bc-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="685bc-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="685bc-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="685bc-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="685bc-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="685bc-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="685bc-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="685bc-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="685bc-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="685bc-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="685bc-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="685bc-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="685bc-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="685bc-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="685bc-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="685bc-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="685bc-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="685bc-140">受信者 3、4、および 5 の受信者リストには、次の順序でプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="685bc-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="685bc-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="685bc-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="685bc-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="685bc-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="685bc-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="685bc-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="685bc-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="685bc-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="685bc-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="685bc-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="685bc-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="685bc-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="685bc-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="685bc-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="685bc-148">**IAddrBook::P repareRecips** を呼び出してプロパティを処理する代わりに、各受信者の [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出し、必要に応じて [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="685bc-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="685bc-149">受信者が 1 人しか関与しない場合は、どちらの方法でも十分です。</span><span class="sxs-lookup"><span data-stu-id="685bc-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="685bc-150">ただし、複数の受信者が関係する場合は **、IMAPIProp** メソッドではなく **PrepareRecips** を呼び出すことによって時間が節約され、リモートで操作している場合は、多くのリモート プロシージャ呼び出しが実行されます。</span><span class="sxs-lookup"><span data-stu-id="685bc-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="685bc-151">**PrepareRecips は** 1 回の呼び出しですべての受信者を処理しますが **、GetProps** と **SetProps** は受信者ごとに 1 回の呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="685bc-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

