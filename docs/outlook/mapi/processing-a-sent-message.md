---
title: 送信されたメッセージの処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 880731bf204778cde21da6cd9024a3ca86c6f6a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434677"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="5e450-103">送信されたメッセージの処理</span><span class="sxs-lookup"><span data-stu-id="5e450-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="5e450-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e450-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e450-105">送信メッセージは送信された後で、送信トレイフォルダーに残したり、送信メッセージを保持するように指定されたフォルダーに移動したり、削除したりできます。</span><span class="sxs-lookup"><span data-stu-id="5e450-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="5e450-106">処理の種類は、メッセージストアのプロパティが設定されているかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="5e450-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="5e450-107">**PR_DELETE_AFTER_SUBMIT**([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5e450-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="5e450-108">**PR_SENTMAIL_ENTRYID**([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5e450-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="5e450-109">**PR_DELETE_AFTER_SUBMIT**はブール型のプロパティで、送信後にメッセージを削除する場合は TRUE に設定し、それ以外の場合は FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="5e450-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="5e450-110">**PR_SENTMAIL_ENTRYID**は、フォルダーのエントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="5e450-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="5e450-111">このプロパティが設定されている場合は、送信されたメッセージをこのエントリ識別子で表されるフォルダーに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e450-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="5e450-112">保存されたメッセージには、通常、それらを送信するための最後のメッセージストアまたはトランスポートプロバイダーの id が設定されます。</span><span class="sxs-lookup"><span data-stu-id="5e450-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="5e450-113">どちらか一方または両方のプロパティを設定する必要はありませんが、両方とも設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="5e450-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="5e450-114">ただし、 **PR_SENTMAIL_ENTRYID**を設定する場合は、有効なエントリ識別子を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e450-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="5e450-115">次の表では、これらのプロパティが送信メッセージの処理に与える影響について説明します。</span><span class="sxs-lookup"><span data-stu-id="5e450-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e450-116">どちらのプロパティも設定されていない場合:</span><span class="sxs-lookup"><span data-stu-id="5e450-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="5e450-117">メッセージを送信元のフォルダー (通常は送信トレイ) に残します。</span><span class="sxs-lookup"><span data-stu-id="5e450-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="5e450-118">**PR_SENTMAIL_ENTRYID**が設定されている場合:</span><span class="sxs-lookup"><span data-stu-id="5e450-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="5e450-119">メッセージを指示されたフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="5e450-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="5e450-120">**PR_DELETE_AFTER_SUBMIT**が設定されている場合:</span><span class="sxs-lookup"><span data-stu-id="5e450-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="5e450-121">メッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="5e450-121">Delete the message.</span></span>  <br/> |
   

