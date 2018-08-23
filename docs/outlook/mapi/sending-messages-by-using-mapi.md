---
title: MAPI を使用したメッセージの送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 36de3b70b0ab7b16f8abed85bbd0983224e00568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803866"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="95b29-103">MAPI を使用したメッセージの送信</span><span class="sxs-lookup"><span data-stu-id="95b29-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="95b29-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95b29-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95b29-105">クライアント アプリケーションは、メッセージを送信する[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="95b29-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="95b29-106">**SubmitMessage**では、MAPI スプーラーを無効にするか、コントロールを転送する前に、またはトランスポート プロバイダーに直接メッセージを保存するのには[IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="95b29-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="95b29-107">MAPI スプーラーは、次のいずれかが発生した場合に、メッセージを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="95b29-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="95b29-108">メッセージ ストア プロバイダーおよびトランスポート プロバイダーが密に結合されていません。</span><span class="sxs-lookup"><span data-stu-id="95b29-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="95b29-109">メッセージには、前処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="95b29-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="95b29-110">密結合のメッセージ ・ ストアおよびトランスポートは、メッセージの宛先は、受信者のすべてで処理できません。</span><span class="sxs-lookup"><span data-stu-id="95b29-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="95b29-111">密結合のメッセージ ・ ストアする必要があります考慮に入れるメッセージのステータス、MAPI スプーラーを無効にするトランスポート プロバイダーをダウンロードするのにはその前に。</span><span class="sxs-lookup"><span data-stu-id="95b29-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="95b29-112">状況で、MAPI スプーラーを要求するメッセージが表示される場合がありますが、MAPI スプーラーを無効する必要があります実際には関与しません。</span><span class="sxs-lookup"><span data-stu-id="95b29-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="95b29-113">たとえば、ユーザーが受信トレイからメッセージを送信する場合があるとします。</span><span class="sxs-lookup"><span data-stu-id="95b29-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="95b29-114">密結合のストアおよびトランスポート、クライアントが使用します。</span><span class="sxs-lookup"><span data-stu-id="95b29-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="95b29-115">密結合のメッセージ ・ ストアでは、唯一の条件としてメッセージの場所を使用して、メッセージを処理するために、MAPI スプーラーを許可するかどうかを決定するため、MAPI スプーラーは常にメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="95b29-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="95b29-116">この種の問題を避けるためには、密結合のメッセージ ・ ストアは、メッセージの場所だけでなくメッセージ状態を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="95b29-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="95b29-117">具体的には、トランスポート プロバイダーを要求しないでください、MAPI スプーラーが積極的に送信されるすべてのメッセージをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="95b29-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="95b29-118">メッセージ ストア プロバイダー、1 つまたは複数のトランスポート プロバイダー、および MAPI メッセージの送信プロセスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="95b29-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="95b29-119">このセクションのトピックでは、メッセージ転送のプロセスで特定の役割に関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="95b29-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95b29-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="95b29-120">See also</span></span>



[<span data-ttu-id="95b29-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="95b29-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="95b29-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="95b29-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

