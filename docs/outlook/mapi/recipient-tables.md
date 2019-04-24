---
title: 受信者テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328421"
---
# <a name="recipient-tables"></a><span data-ttu-id="b6e78-103">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="b6e78-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="b6e78-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6e78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6e78-105">recipient テーブルには、メッセージのすべての受信者に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b6e78-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="b6e78-106">メッセージストアプロバイダーは受信者テーブルを実装し、クライアントアプリケーションはそれらを使用します。</span><span class="sxs-lookup"><span data-stu-id="b6e78-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="b6e78-107">クライアントは、 [IMessage:: get table](imessage-getrecipienttable.md)メソッドを呼び出して、またはメッセージストアプロバイダーが[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドに対してサポートしている場合に、受信者テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="b6e78-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="b6e78-108">クライアントは、プロパティタグおよび IID_IMAPITable のインターフェイス識別子に対して**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) を指定することによって、 **openproperty**を使用して受信者テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="b6e78-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="b6e78-109">受信者テーブルへの変更は、 [IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドを呼び出すことで行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b6e78-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="b6e78-110">受信者テーブルは、メッセージが送信されたかどうかに応じて異なる列セットを持ちます。</span><span class="sxs-lookup"><span data-stu-id="b6e78-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="b6e78-111">次のプロパティを使用して、受信者テーブルで必要な列セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="b6e78-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="b6e78-112">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6e78-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="b6e78-113">**PR_RECIPIENT_TYPE**([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6e78-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="b6e78-114">**PR_ROWID**([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6e78-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="b6e78-115">オプションのプロパティは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b6e78-115">The optional properties are:</span></span>
  
- <span data-ttu-id="b6e78-116">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6e78-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="b6e78-117">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6e78-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="b6e78-118">**PR_SPOOLER_STATUS**([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6e78-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="b6e78-119">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6e78-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="b6e78-120">送信されたメッセージには、必要な列セットにこれらの追加プロパティが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6e78-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="b6e78-121">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6e78-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="b6e78-122">**PR_RESPONSIBILITY**([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6e78-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="b6e78-123">プロバイダーの実装によっては、 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) や[ENTRYID](entryid.md)などの追加の列がテーブルに含まれることがあります。</span><span class="sxs-lookup"><span data-stu-id="b6e78-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="b6e78-124">プロバイダーの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで設定されている STORE_SUBMIT_OK ビットによって示されるように、メッセージ転送をサポートするメッセージストアプロバイダーは、特定のセットののサポートを提供する必要があります。受信者テーブルの実装での制限。</span><span class="sxs-lookup"><span data-stu-id="b6e78-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="b6e78-125">**and**、 **OR**、exist、およびプロパティの制限は、受信者テーブルのユーザーが使用できるようにする制限の種類の中にあります。</span><span class="sxs-lookup"><span data-stu-id="b6e78-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="b6e78-126">プロパティ制限で同等および等しくない演算子のみをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6e78-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="b6e78-127">これらの制限は、次のプロパティで機能する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6e78-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="b6e78-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="b6e78-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="b6e78-129">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b6e78-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="b6e78-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="b6e78-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="b6e78-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="b6e78-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="b6e78-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="b6e78-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6e78-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6e78-133">See also</span></span>



[<span data-ttu-id="b6e78-134">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="b6e78-134">MAPI Tables</span></span>](mapi-tables.md)

