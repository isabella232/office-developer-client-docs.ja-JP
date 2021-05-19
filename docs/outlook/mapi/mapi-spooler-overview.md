---
title: MAPI スプーラーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 162957ea17b5a82d4da68340e971d328c85cd9f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432717"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="3ddbc-103">MAPI スプーラーの概要</span><span class="sxs-lookup"><span data-stu-id="3ddbc-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="3ddbc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ddbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ddbc-105">MAPI スプーラーは、メッセージング システムMicrosoft Office Outlookメッセージの送受信を行うプロセスの関数です。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="3ddbc-106">MAPI スプーラーは、メッセージの受信と配信において重要な役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="3ddbc-107">メッセージング システムが使用できない場合、MAPI スプーラーはメッセージを保存し、後で自動的に転送します。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="3ddbc-108">必要に応じてデータを保持または送信する機能は、リモート接続が一般的でネットワーク トラフィックが多い環境で重要な機能であるストアと転送と呼ばれる機能です。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="3ddbc-109">MAPI スプーラーは、アプリ内でバックグラウンド スレッドOutlook。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="3ddbc-110">MAPI スプーラーには、メッセージの配布に関連する追加の責任があります。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="3ddbc-111">これらの追加の職務には、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="3ddbc-112">特定のトランスポート プロバイダーによって処理される受信者の種類を追跡します。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="3ddbc-113">新しいメッセージが配信された場合にクライアント アプリケーションに通知します。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="3ddbc-114">メッセージの前処理と後処理の呼び出し。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="3ddbc-115">メッセージ配信が発生したというレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="3ddbc-116">処理された受信者の状態を維持する。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="3ddbc-117">次の図は、メッセージがクライアントからメッセージング システムに流れる方法を高レベルで示しています。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="3ddbc-118">**出力メッセージ フロー**</span><span class="sxs-lookup"><span data-stu-id="3ddbc-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="3ddbc-119">![送信メッセージ フロー](media/amapi_46.gif "送信メッセージ フロー")</span><span class="sxs-lookup"><span data-stu-id="3ddbc-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="3ddbc-120">クライアント アプリケーションのユーザーは、1 つ以上の受信者にメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="3ddbc-121">メッセージ ストア プロバイダーは送信プロセスを開始し、送信に必要な追加情報を含むメッセージを書式設定します。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="3ddbc-122">MAPI スプーラーは、次の条件が発生した場合に処理するメッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="3ddbc-123">メッセージ ストア プロバイダーは、トランスポート プロバイダーと密に結合されません。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="3ddbc-124">メッセージには前処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="3ddbc-125">メッセージ ストアとトランスポート プロバイダーは緊密に結合されますが、メッセージの宛先であるすべての受信者を処理することはできません。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="3ddbc-126">MAPI スプーラーがメッセージを受信すると、必要な前処理が実行され、適切なトランスポート プロバイダーにメッセージが配信されます。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="3ddbc-127">トランスポート プロバイダーはメッセージをメッセージング システムに送信し、メッセージを目的の受信者に送信します。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="3ddbc-128">受信メッセージを使用すると、フローは元に戻されます。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="3ddbc-129">トランスポート プロバイダーは、メッセージング システムからメッセージを受信し、MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="3ddbc-130">スプーラーは必要な後処理を実行し、新しいメッセージが到着したメッセージ ストア プロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="3ddbc-131">この通知により、クライアントはメッセージ表示を更新し、ユーザーが新しいメッセージを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="3ddbc-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3ddbc-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ddbc-132">See also</span></span>

- [<span data-ttu-id="3ddbc-133">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="3ddbc-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

