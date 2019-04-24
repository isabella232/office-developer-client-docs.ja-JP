---
title: MAPI を使用してメッセージを送信する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf6324b89f06ef7f0553d3de1eaa24ae31a329ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339754"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="1af33-103">MAPI を使用してメッセージを送信する</span><span class="sxs-lookup"><span data-stu-id="1af33-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="1af33-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1af33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1af33-105">クライアントアプリケーションは、 [IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出して、メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="1af33-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="1af33-106">**submitmessage**呼び出し[imapiprop:: SaveChanges](imapiprop-savechanges.md)は、コントロールを MAPI スプーラーまたはトランスポートプロバイダーに直接転送する前にメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="1af33-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="1af33-107">MAPI スプーラーは、次のいずれかが発生した場合にメッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="1af33-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="1af33-108">メッセージストアプロバイダーとトランスポートプロバイダーは密接に結合されていません。</span><span class="sxs-lookup"><span data-stu-id="1af33-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="1af33-109">メッセージには前処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="1af33-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="1af33-110">密結合メッセージストアとトランスポートは、メッセージの宛先になっているすべての受信者を処理できません。</span><span class="sxs-lookup"><span data-stu-id="1af33-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="1af33-111">密結合メッセージストアは、メッセージの状態を、MAPI スプーラーに送信してトランスポートプロバイダーにダウンロードする前に、そのメッセージの状態を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af33-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="1af33-112">mapi スプーラーを必要とするメッセージが表示される場合がありますが、mapi スプーラーは実際には関係ありません。</span><span class="sxs-lookup"><span data-stu-id="1af33-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="1af33-113">たとえば、ユーザーが受信トレイからメッセージを送信する状況を考えてみます。</span><span class="sxs-lookup"><span data-stu-id="1af33-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="1af33-114">クライアントは、密結合ストアとトランスポートを使用しています。</span><span class="sxs-lookup"><span data-stu-id="1af33-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="1af33-115">密結合メッセージストアがメッセージの場所を使用して、mapi スプーラーによるメッセージの処理を許可するかどうかを決定するための唯一の条件として、mapi スプーラーは常にメッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="1af33-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="1af33-116">この種の問題を回避するには、密結合のメッセージストアで、メッセージの場所に加えてメッセージの状態を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1af33-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="1af33-117">具体的には、トランスポートプロバイダーは、MAPI スプーラーが送信中のメッセージをダウンロードすることを要求してはなりません。</span><span class="sxs-lookup"><span data-stu-id="1af33-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="1af33-118">メッセージ転送プロセスには、メッセージストアプロバイダー、1つ以上のトランスポートプロバイダー、MAPI が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1af33-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="1af33-119">このセクションのトピックでは、メッセージ送信プロセスにおける特定の役割について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="1af33-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1af33-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="1af33-120">See also</span></span>



[<span data-ttu-id="1af33-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="1af33-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="1af33-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="1af33-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

