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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309582"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="f580b-103">MAPI スプーラーの概要</span><span class="sxs-lookup"><span data-stu-id="f580b-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="f580b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f580b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f580b-105">MAPI スプーラーは、メッセージングシステムとの間でメッセージの送受信を行う Microsoft Office Outlook プロセスの機能です。</span><span class="sxs-lookup"><span data-stu-id="f580b-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="f580b-106">MAPI スプーラーは、メッセージの受信と配信で重要な役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="f580b-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="f580b-107">メッセージングシステムが使用できなくなると、MAPI スプーラーはメッセージを保存し、後で自動的に転送します。</span><span class="sxs-lookup"><span data-stu-id="f580b-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="f580b-108">必要に応じてデータを保持または送信できるようにする機能は、「ストアアンドフォワード」と呼ばれていますが、リモート接続が共通でネットワークトラフィックが多い環境で重要な機能です。</span><span class="sxs-lookup"><span data-stu-id="f580b-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="f580b-109">MAPI スプーラーは、Outlook 内でバックグラウンドスレッドとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="f580b-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="f580b-110">MAPI スプーラーには、メッセージの配布に関連する追加の責任があります。</span><span class="sxs-lookup"><span data-stu-id="f580b-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="f580b-111">これらの追加の職務には、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="f580b-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="f580b-112">特定のトランスポートプロバイダーによって処理される受信者の種類を追跡します。</span><span class="sxs-lookup"><span data-stu-id="f580b-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="f580b-113">新しいメッセージが配信されたときに、クライアントアプリケーションに通知します。</span><span class="sxs-lookup"><span data-stu-id="f580b-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="f580b-114">メッセージ前処理と後処理を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f580b-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="f580b-115">メッセージ配信が発生したことを示すレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="f580b-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="f580b-116">処理された受信者の状態を維持します。</span><span class="sxs-lookup"><span data-stu-id="f580b-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="f580b-117">次の図は、メッセージがクライアントからメッセージングシステムに送られる方法の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="f580b-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="f580b-118">**出力メッセージ フロー**</span><span class="sxs-lookup"><span data-stu-id="f580b-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="f580b-119">![送信メッセージフロー](media/amapi_46.gif "送信メッセージフロー")</span><span class="sxs-lookup"><span data-stu-id="f580b-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="f580b-120">クライアントアプリケーションのユーザーが1人以上の受信者にメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="f580b-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="f580b-121">メッセージストアプロバイダーが送信プロセスを開始し、送信に必要な追加情報をメッセージに書式設定します。</span><span class="sxs-lookup"><span data-stu-id="f580b-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="f580b-122">MAPI スプーラーは、次のいずれかの状況が発生した場合に処理するメッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="f580b-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="f580b-123">メッセージストアプロバイダーがトランスポートプロバイダーと密接に結合されていません。</span><span class="sxs-lookup"><span data-stu-id="f580b-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="f580b-124">メッセージには前処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="f580b-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="f580b-125">メッセージストアとトランスポートプロバイダーは密接に結合されていますが、メッセージの宛先になっているすべての受信者を処理することはできません。</span><span class="sxs-lookup"><span data-stu-id="f580b-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="f580b-126">MAPI スプーラーは、メッセージを受信すると、必要な前処理を実行し、適切なトランスポートプロバイダーにメッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="f580b-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="f580b-127">トランスポートプロバイダーは、メッセージをメッセージングシステムに渡します。メッセージは、目的の受信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="f580b-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="f580b-128">受信メッセージの場合、フローは取り消されます。</span><span class="sxs-lookup"><span data-stu-id="f580b-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="f580b-129">トランスポートプロバイダーは、メッセージングシステムからメッセージを受信し、MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="f580b-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="f580b-130">スプーラーは必要な後処理を実行し、新しいメッセージが到着したことをメッセージストアプロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="f580b-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="f580b-131">この通知により、クライアントはメッセージの表示を更新し、ユーザーが新しいメッセージを読むことができるようになります。</span><span class="sxs-lookup"><span data-stu-id="f580b-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f580b-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="f580b-132">See also</span></span>

- [<span data-ttu-id="f580b-133">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="f580b-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

