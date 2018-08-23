---
title: 送信したメッセージの処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0cea1a1008ecbff698b757d6c67af5c279954656
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803677"
---
# <a name="processing-a-sent-message"></a><span data-ttu-id="47a39-103">送信したメッセージの処理</span><span class="sxs-lookup"><span data-stu-id="47a39-103">Processing a Sent Message</span></span>

  
  
<span data-ttu-id="47a39-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47a39-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47a39-105">それらが送信された後、送信メッセージの数をおくことができますを保持するために指定されたフォルダーに移動されているフォルダーは、メッセージを送信または削除、[送信トレイ] にします。</span><span class="sxs-lookup"><span data-stu-id="47a39-105">Outgoing messages, after they have been sent, can be left in the Outbox folder, moved to a folder designated to hold sent messages, or deleted.</span></span> <span data-ttu-id="47a39-106">処理の種類は、かどうか設定したメッセージ ・ ストア ・ プロパティによって異なります。</span><span class="sxs-lookup"><span data-stu-id="47a39-106">The type of processing depends on whether or not you have set the message store properties:</span></span>
  
- <span data-ttu-id="47a39-107">**PR_DELETE_AFTER_SUBMIT**([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="47a39-107">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span> 
    
- <span data-ttu-id="47a39-108">**PR_SENTMAIL_ENTRYID**([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="47a39-108">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span> 
    
 <span data-ttu-id="47a39-109">**PR_DELETE_AFTER_SUBMIT**は、それ以外の場合、送信後にメッセージを削除する場合は TRUE、FALSE に設定、ブール型プロパティです。</span><span class="sxs-lookup"><span data-stu-id="47a39-109">**PR_DELETE_AFTER_SUBMIT** is a Boolean property, set to TRUE if messages should be deleted after they are sent, and FALSE otherwise.</span></span> <span data-ttu-id="47a39-110">**PR_SENTMAIL_ENTRYID**は、フォルダーのエントリ id です。</span><span class="sxs-lookup"><span data-stu-id="47a39-110">**PR_SENTMAIL_ENTRYID** is the entry identifier of a folder.</span></span> <span data-ttu-id="47a39-111">このプロパティを設定すると、このエントリの識別子によって表されるフォルダーに送信したメッセージを移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47a39-111">When this property is set, you should move sent messages to the folder represented by this entry identifier.</span></span> <span data-ttu-id="47a39-112">保存されたメッセージは通常の最後のメッセージ ・ ストア id を持っているか、転送を送信するプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="47a39-112">The saved messages typically have the identity of the last message store or transport provider to send them.</span></span> 
  
<span data-ttu-id="47a39-113">セット、両方ではありませんが、いずれか 1 つ、またはこれらのプロパティのどちらも必要があります。</span><span class="sxs-lookup"><span data-stu-id="47a39-113">Either one or the other, or neither of these properties should be set, but not both.</span></span> <span data-ttu-id="47a39-114">ただし、 **PR_SENTMAIL_ENTRYID**を設定した場合、有効なエントリの識別子を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="47a39-114">However, if you set **PR_SENTMAIL_ENTRYID**, it must contain a valid entry identifier.</span></span> 
  
<span data-ttu-id="47a39-115">次の表は、どのようにこれらのプロパティに影響を与える送信メッセージに対して行う操作について説明します。</span><span class="sxs-lookup"><span data-stu-id="47a39-115">The following table describes how these properties affect what you do with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47a39-116">場合は 2 つのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="47a39-116">If neither property is set:</span></span>  <br/> |<span data-ttu-id="47a39-117">(通常、[送信トレイ]) の送信、元のフォルダーにメッセージを残します。</span><span class="sxs-lookup"><span data-stu-id="47a39-117">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="47a39-118">場合は**PR_SENTMAIL_ENTRYID**が設定されます。</span><span class="sxs-lookup"><span data-stu-id="47a39-118">If **PR_SENTMAIL_ENTRYID** is set:</span></span>  <br/> |<span data-ttu-id="47a39-119">指定されたフォルダーにメッセージを移動します。</span><span class="sxs-lookup"><span data-stu-id="47a39-119">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="47a39-120">場合は**PR_DELETE_AFTER_SUBMIT**が設定されます。</span><span class="sxs-lookup"><span data-stu-id="47a39-120">If **PR_DELETE_AFTER_SUBMIT** is set:</span></span>  <br/> |<span data-ttu-id="47a39-121">メッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="47a39-121">Delete the message.</span></span>  <br/> |
   

