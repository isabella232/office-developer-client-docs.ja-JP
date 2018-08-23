---
title: 受信者テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cc7635c474b99898d59589f33fcf06cf24697378
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803722"
---
# <a name="recipient-tables"></a><span data-ttu-id="a789f-103">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="a789f-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="a789f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a789f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a789f-105">受信者テーブルには、メッセージのすべての受信者に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a789f-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="a789f-106">メッセージ ストア プロバイダーは、受信者テーブルを実装し、クライアント アプリケーションが使用します。</span><span class="sxs-lookup"><span data-stu-id="a789f-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="a789f-107">クライアントは、 [IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを呼び出すことによって受信者テーブルにアクセスまたは場合は、メッセージ ・ ストア プロバイダーでサポートされている、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドにします。</span><span class="sxs-lookup"><span data-stu-id="a789f-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="a789f-108">インターフェイス識別子のプロパティ タグと IID_IMAPITable の**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) を指定することによって**OpenProperty**を持つ受信者テーブルをクライアントにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="a789f-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="a789f-109">受信者テーブルへの変更は、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを呼び出すことによって可能です。</span><span class="sxs-lookup"><span data-stu-id="a789f-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="a789f-110">受信者テーブルには、メッセージが送信されたかどうかに応じて、設定の異なる列があります。</span><span class="sxs-lookup"><span data-stu-id="a789f-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="a789f-111">次のプロパティは、受信者テーブルの設定の必要な列を構成します。</span><span class="sxs-lookup"><span data-stu-id="a789f-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="a789f-112">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a789f-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="a789f-113">**PR_RECIPIENT_TYPE**([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a789f-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="a789f-114">**PR_ROWID**([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a789f-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="a789f-115">省略可能なプロパティは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a789f-115">The optional properties are:</span></span>
  
- <span data-ttu-id="a789f-116">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a789f-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="a789f-117">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a789f-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="a789f-118">**PR_SPOOLER_STATUS**([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a789f-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="a789f-119">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a789f-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="a789f-120">送信されたメッセージは、必要な列のセットに追加したプロパティを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="a789f-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="a789f-121">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a789f-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="a789f-122">**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a789f-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="a789f-123">プロバイダーの実装では、によって、テーブルの[エントリ ID](entryid.md)、 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) などの追加の列があります。</span><span class="sxs-lookup"><span data-stu-id="a789f-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="a789f-124">メッセージの送信をサポートする任意のメッセージ ストア プロバイダー、プロバイダーの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティに設定されている STORE_SUBMIT_OK ビットによって示されるなどの特定のセットのサポートを提供する必要があります受信者テーブルの実装で制限します。</span><span class="sxs-lookup"><span data-stu-id="a789f-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="a789f-125">****、**または**、次のように存在して、プロパティの制限は、受信者テーブルのユーザーが使用可能にする必要がある制限の種類。</span><span class="sxs-lookup"><span data-stu-id="a789f-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="a789f-126">のみ、等しいと等しくない演算子は、プロパティの制限をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a789f-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="a789f-127">これらの制限は、次のプロパティを操作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a789f-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="a789f-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="a789f-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="a789f-129">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a789f-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="a789f-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="a789f-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="a789f-131">**れない**</span><span class="sxs-lookup"><span data-stu-id="a789f-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="a789f-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="a789f-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a789f-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="a789f-133">See also</span></span>



[<span data-ttu-id="a789f-134">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="a789f-134">MAPI Tables</span></span>](mapi-tables.md)

