---
title: 送信メッセージの処理
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
# <a name="processing-a-sent-message"></a><span data-ttu-id="4fa1a-103">送信メッセージの処理</span><span class="sxs-lookup"><span data-stu-id="4fa1a-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="4fa1a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fa1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fa1a-105">送信メッセージは、送信後に送信ボックス フォルダーに残したり、送信済みメッセージを保持するために指定されたフォルダーに移動したり、削除したりできます。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="4fa1a-106">処理の種類は、メッセージ ストアのプロパティを設定したかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="4fa1a-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4fa1a-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="4fa1a-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4fa1a-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="4fa1a-109">**PR_DELETE_AFTER_SUBMIT** はブール型 (Boolean) のプロパティで、メッセージが送信された後に削除する必要がある場合は TRUE に設定され、それ以外の場合は FALSE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="4fa1a-110">**PR_SENTMAIL_ENTRYID** は、フォルダーのエントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="4fa1a-111">このプロパティを設定すると、送信されたメッセージをこのエントリ識別子で表されるフォルダーに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="4fa1a-112">保存されたメッセージは、通常、最後に送信するメッセージ ストアまたはトランスポート プロバイダーの ID を持っています。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="4fa1a-113">どちらか一方または他のプロパティを設定するか、これらのプロパティのどちらも設定する必要がありますが、両方を設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="4fa1a-114">ただし、この値を設定 **PR_SENTMAIL_ENTRYID、** 有効なエントリ識別子が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="4fa1a-115">次の表では、これらのプロパティが送信メッセージの処理に与える影響について説明します。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4fa1a-116">どちらのプロパティも設定しない場合:</span><span class="sxs-lookup"><span data-stu-id="4fa1a-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="4fa1a-117">メッセージは、送信されたフォルダー (通常は送信箱) に残します。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="4fa1a-118">この **PR_SENTMAIL_ENTRYID** 設定されている場合は、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="4fa1a-119">メッセージを指定したフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="4fa1a-120">この **PR_DELETE_AFTER_SUBMIT** 設定されている場合は、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="4fa1a-121">メッセージを削除する。</span><span class="sxs-lookup"><span data-stu-id="4fa1a-121">Delete the message.</span></span>  <br/> |
   

