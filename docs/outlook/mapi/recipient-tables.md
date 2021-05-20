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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437288"
---
# <a name="recipient-tables"></a><span data-ttu-id="d64d6-103">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="d64d6-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="d64d6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d64d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d64d6-105">受信者テーブルには、メッセージのすべての受信者に関する情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d64d6-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="d64d6-106">メッセージ ストア プロバイダーは受信者テーブルを実装し、クライアント アプリケーションはそれらを使用します。</span><span class="sxs-lookup"><span data-stu-id="d64d6-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="d64d6-107">[クライアントは、IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを呼び出して受信者テーブルにアクセスするか、メッセージ ストア プロバイダーがそれをサポートしている場合は[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d64d6-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="d64d6-108">クライアントは、プロパティ タグに **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) を指定し、インターフェイス識別子に IID_IMAPITable を指定して **、OpenProperty** を使用して受信者テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d64d6-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="d64d6-109">受信者テーブルに対する変更は [、IMessage::ModifyRecipients](imessage-modifyrecipients.md) メソッドを呼び出すことによって行えます。</span><span class="sxs-lookup"><span data-stu-id="d64d6-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="d64d6-110">受信者テーブルの列セットは、メッセージが送信されたかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="d64d6-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="d64d6-111">次のプロパティは、受信者テーブルで必要な列セットを構成します。</span><span class="sxs-lookup"><span data-stu-id="d64d6-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="d64d6-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d64d6-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="d64d6-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d64d6-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="d64d6-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d64d6-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="d64d6-115">オプションのプロパティは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d64d6-115">The optional properties are:</span></span>
  
- <span data-ttu-id="d64d6-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d64d6-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="d64d6-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d64d6-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="d64d6-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d64d6-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="d64d6-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d64d6-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="d64d6-120">送信されたメッセージには、次の追加プロパティを必須の列セットに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d64d6-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="d64d6-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d64d6-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="d64d6-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d64d6-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="d64d6-123">プロバイダーの実装によっては、PR_SENDER_NAME **(** [PidTagSenderName](pidtagsendername-canonical-property.md)) や [ENTRYID](entryid.md)などの追加の列が表に含まれます。</span><span class="sxs-lookup"><span data-stu-id="d64d6-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="d64d6-124">プロバイダー **の PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)プロパティで設定されている STORE_SUBMIT_OK ビットによって示されるメッセージ送信をサポートするメッセージ ストア プロバイダーは、受信者テーブルの実装における特定の制限セットをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d64d6-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="d64d6-125">**AND** **、OR、** およびプロパティの制限は、受信者テーブルのユーザーが使用できる制限の種類の中にあります。</span><span class="sxs-lookup"><span data-stu-id="d64d6-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="d64d6-126">プロパティの制限では、等しい演算子と等しくない演算子のみをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d64d6-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="d64d6-127">これらの制限は、次のプロパティで動作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d64d6-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="d64d6-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="d64d6-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="d64d6-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d64d6-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="d64d6-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="d64d6-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="d64d6-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="d64d6-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="d64d6-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="d64d6-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d64d6-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="d64d6-133">See also</span></span>



[<span data-ttu-id="d64d6-134">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="d64d6-134">MAPI Tables</span></span>](mapi-tables.md)

