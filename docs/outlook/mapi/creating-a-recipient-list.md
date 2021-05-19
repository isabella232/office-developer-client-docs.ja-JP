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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428215"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="66634-103">受信者リストの作成</span><span class="sxs-lookup"><span data-stu-id="66634-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="66634-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66634-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66634-105">受信者リストは、メッセージの宛先である各メッセージ受信者のプロパティ値構造の配列を含む [ADRLIST](adrlist.md) 構造体です。</span><span class="sxs-lookup"><span data-stu-id="66634-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="66634-106">受信者は、人間のユーザー、コンピューター、またはフォルダーを表します。</span><span class="sxs-lookup"><span data-stu-id="66634-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="66634-107">送信するメッセージはすべて、名前解決プロセスを実行した少なくとも 1 人の受信者を必要とします **。つまり、PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが受信者のプロパティ値配列に含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="66634-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="66634-108">受信者のプロパティは、アドレス帳プロパティとメッセージ プロパティの組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="66634-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="66634-109">受信者プロパティは、特定の受信者のすべてのメッセージに適用するか、現在のメッセージにのみ適用できます。</span><span class="sxs-lookup"><span data-stu-id="66634-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="66634-110">メッセージ ストアとトランスポート プロバイダーの両方で受信者のプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="66634-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="66634-111">各受信者は、メッセージを送信する準備が整うまで、プロパティ値配列内のプロパティのコア セットを持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="66634-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="66634-112">必要な受信者プロパティのセットは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="66634-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="66634-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66634-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="66634-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66634-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="66634-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66634-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="66634-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="66634-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="66634-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66634-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="66634-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66634-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="66634-119">これらのプロパティは、受信者にアクセスし、メッセージを送信し、他のユーザーと比較するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="66634-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="66634-120">これらのプロパティのすべては、すぐ利用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="66634-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="66634-121">このプロパティを割り当てるには、名前解決プロセスに依存して、エントリ識別子を知らなくても、最初に受信者を追加できます。</span><span class="sxs-lookup"><span data-stu-id="66634-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="66634-122">メッセージを送信する前に [、IAddrBook::ResolveName](iaddrbook-resolvename.md) を呼び出して、受信者リスト内のすべての受信者が解決されるのを確認します。</span><span class="sxs-lookup"><span data-stu-id="66634-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="66634-123">詳細については、「受信者名の [解決」を参照してください](resolving-a-recipient-name.md)。</span><span class="sxs-lookup"><span data-stu-id="66634-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="66634-124">受信者リストは、メッセージング ユーザーまたはアドレス帳コンテナー内の配布リスト エントリ、または 1 回きりから作成できます。</span><span class="sxs-lookup"><span data-stu-id="66634-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="66634-125">1 回限りは、1 つのメッセージへのアドレス指定にのみ使用する一時的なエントリとして作成される受信者、または個人用アドレス帳に追加するエントリとして作成される受信者です。</span><span class="sxs-lookup"><span data-stu-id="66634-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="66634-126">1 回のエントリ識別子とアドレスの形式は、MAPI によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="66634-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="66634-127">これらの形式の詳細については [、「One-Off Addresses and](one-off-addresses.md) [One-Off Entry IDENTIFIERs」を参照してください](one-off-entry-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="66634-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="66634-128">ユーザーが受信者リストを作成できます。</span><span class="sxs-lookup"><span data-stu-id="66634-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="66634-129">アドレス帳からのエントリがある場合のみ。</span><span class="sxs-lookup"><span data-stu-id="66634-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="66634-130">1 回限定のエントリの場合のみ。</span><span class="sxs-lookup"><span data-stu-id="66634-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="66634-131">アドレス帳の受信者と 1 回きりを組み合わせて使用します。</span><span class="sxs-lookup"><span data-stu-id="66634-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="66634-132">**[共通アドレス] ダイアログ ボックスを使用して受信者リストを作成するには**</span><span class="sxs-lookup"><span data-stu-id="66634-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="66634-133">[ADRPARM 構造体と ADRLIST](adrparm.md)構造体へのポインター[を割り当](adrlist.md)てる。</span><span class="sxs-lookup"><span data-stu-id="66634-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="66634-134">**ADRPARM 構造体のメモリを 0 に** し **、ADRLIST** ポインターを NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="66634-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="66634-135">[IAddrBook::Address を](iaddrbook-address.md)呼び出して、アドレス ダイアログ ボックスを表示し **、ADRPARM 構造を設定** します。</span><span class="sxs-lookup"><span data-stu-id="66634-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="66634-136">[IMessage::ModifyRecipients を呼び出し](imessage-modifyrecipients.md)**、ADRLIST ポインターを渡** します。</span><span class="sxs-lookup"><span data-stu-id="66634-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="66634-137">この構造には、ユーザーが選択した各受信者のプロパティが含まれる。</span><span class="sxs-lookup"><span data-stu-id="66634-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="66634-138">**受信者リストをプログラムで作成するには**</span><span class="sxs-lookup"><span data-stu-id="66634-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="66634-139">リストに **含める受信者ごとに** [1 つの ADRENTRY](adrentry.md) 構造を含む ADRLIST 構造を割り当てる。</span><span class="sxs-lookup"><span data-stu-id="66634-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="66634-140">各 **ADRENTRY 構造を、** 必要なプロパティとプロパティ [(PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)を保持するのに十分な **PR_RECIPIENT_TYPE** してください。</span><span class="sxs-lookup"><span data-stu-id="66634-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="66634-141">受信者ごとに **、ADRLIST** 構造体の **aEntries** メンバーのプロパティ値配列を設定します。</span><span class="sxs-lookup"><span data-stu-id="66634-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="66634-142">[IMessage::ModifyRecipients](imessage-modifyrecipients.md)を呼び出し、MODRECIP_ADD設定します。</span><span class="sxs-lookup"><span data-stu-id="66634-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

