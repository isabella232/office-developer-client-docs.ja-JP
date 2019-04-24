---
title: 受信者リストの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e3aa1f2b2e1e7c6d8a9be3fff451002952930ffb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332908"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="e7d93-103">受信者リストの作成</span><span class="sxs-lookup"><span data-stu-id="e7d93-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="e7d93-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7d93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7d93-105">受信者リストは、各メッセージ受信者のプロパティ値構造 (メッセージの送信先) の配列を含む[adrlist](adrlist.md)構造です。</span><span class="sxs-lookup"><span data-stu-id="e7d93-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="e7d93-106">受信者は、人間のユーザー、コンピューター、またはフォルダーを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="e7d93-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="e7d93-107">送信されるすべてのメッセージには、名前解決プロセスを通じて、少なくとも1人の受信者が必要です。 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが受信者のプロパティ値配列に含まれていることを確認するプロセスです。</span><span class="sxs-lookup"><span data-stu-id="e7d93-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="e7d93-108">受信者のプロパティは、アドレス帳のプロパティとメッセージのプロパティの組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="e7d93-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="e7d93-109">受信者のプロパティは、特定の受信者のすべてのメッセージに適用するか、または現在のメッセージのみに適用することができます。</span><span class="sxs-lookup"><span data-stu-id="e7d93-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="e7d93-110">メッセージストアプロバイダーとトランスポートプロバイダーは、どちらも受信者プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e7d93-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="e7d93-111">各受信者は、メッセージの送信の準備ができたときに、プロパティの値の配列にプロパティのコアセットを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7d93-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="e7d93-112">必要な受信者プロパティのセットは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e7d93-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="e7d93-113">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e7d93-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="e7d93-114">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e7d93-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="e7d93-115">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e7d93-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="e7d93-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="e7d93-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="e7d93-117">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e7d93-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="e7d93-118">**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e7d93-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="e7d93-119">これらのプロパティは、受信者へのアクセス、メッセージの送信、および他のユーザーとの比較に使用されます。</span><span class="sxs-lookup"><span data-stu-id="e7d93-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="e7d93-120">これらのプロパティの一部は、すぐに使用できるようにする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e7d93-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="e7d93-121">このプロパティを割り当てるには、名前解決プロセスに依存して、エントリ id を知らなくても受信者を最初に追加できます。</span><span class="sxs-lookup"><span data-stu-id="e7d93-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="e7d93-122">メッセージを送信する前に、ある時点で、 [IAddrBook:: ResolveName](iaddrbook-resolvename.md)を呼び出して、受信者一覧のすべての受信者が解決されるようにします。</span><span class="sxs-lookup"><span data-stu-id="e7d93-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="e7d93-123">詳細については、「[受信者名の解決](resolving-a-recipient-name.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7d93-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="e7d93-124">受信者リストは、アドレス帳コンテナー内のメッセージングユーザーまたは配布リストのエントリから、または1回から作成できます。</span><span class="sxs-lookup"><span data-stu-id="e7d93-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="e7d93-125">1回限りの受信者は、1つのメッセージのアドレス指定にのみ使用される一時エントリ、または個人用アドレス帳に追加されるエントリとして作成される受信者です。</span><span class="sxs-lookup"><span data-stu-id="e7d93-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="e7d93-126">1回限りのエントリ id とアドレスの形式は、MAPI によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="e7d93-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="e7d93-127">これらの形式の詳細については、「 [1 回限りのアドレス](one-off-addresses.md)と[1 回限りのエントリ識別子](one-off-entry-identifiers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7d93-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="e7d93-128">ユーザーが受信者リストを作成できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e7d93-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="e7d93-129">アドレス帳のエントリのみを使用します。</span><span class="sxs-lookup"><span data-stu-id="e7d93-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="e7d93-130">1回限りのエントリのみを使用します。</span><span class="sxs-lookup"><span data-stu-id="e7d93-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="e7d93-131">アドレス帳の受信者と1回の組み合わせの組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="e7d93-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="e7d93-132">**[共通アドレス] ダイアログボックスを使用して受信者リストを作成するには**</span><span class="sxs-lookup"><span data-stu-id="e7d93-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="e7d93-133">[ADRPARM](adrparm.md)構造体と[adrlist](adrlist.md)構造体へのポインターを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e7d93-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="e7d93-134">**ADRPARM**構造体のメモリをゼロにし、 **adrlist**ポインターを NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="e7d93-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="e7d93-135">[IAddrBook:: address](iaddrbook-address.md)を呼び出して、[アドレス] ダイアログボックスを表示し、 **ADRPARM**構造を設定します。</span><span class="sxs-lookup"><span data-stu-id="e7d93-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="e7d93-136">[IMessage:: modifyrecipients](imessage-modifyrecipients.md)を呼び出し、 **adrlist**ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="e7d93-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="e7d93-137">この構造体には、ユーザーによって選択された各受信者のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e7d93-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="e7d93-138">**プログラムで受信者リストを作成するには**</span><span class="sxs-lookup"><span data-stu-id="e7d93-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="e7d93-139">リストに含める受信者ごとに1つの[adrlist](adrentry.md)構造を含む**adrlist**構造を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e7d93-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="e7d93-140">各**adrentry**構造を、必要なプロパティと**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) を保持するために十分な大きさにします。</span><span class="sxs-lookup"><span data-stu-id="e7d93-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="e7d93-141">各受信者について、 **adrlist**構造の**aentries**メンバーにプロパティ値の配列を設定します。</span><span class="sxs-lookup"><span data-stu-id="e7d93-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="e7d93-142">MODRECIP_ADD フラグが設定されている[IMessage:: modifyrecipients](imessage-modifyrecipients.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e7d93-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

