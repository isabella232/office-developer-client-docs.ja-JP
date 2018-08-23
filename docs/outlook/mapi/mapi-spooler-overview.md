---
title: MAPI スプーラーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5e4bd4f6038db3dbb33ec3511d953448fea7a6c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801468"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="fd278-103">MAPI スプーラーの概要</span><span class="sxs-lookup"><span data-stu-id="fd278-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="fd278-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd278-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd278-105">MAPI スプーラーは、Microsoft Office Outlook プロセスが担当するへのメッセージ送信と受信メッセージのメッセージング システムからの機能です。</span><span class="sxs-lookup"><span data-stu-id="fd278-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="fd278-106">MAPI スプーラーは、メッセージの受信と配信で重要な役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="fd278-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="fd278-107">メッセージング システムが使用できない場合は、MAPI スプーラーはメッセージを格納し、後でそれらが自動的に転送します。</span><span class="sxs-lookup"><span data-stu-id="fd278-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="fd278-108">上に保持または、必要に応じてデータを送信するには、この機能は、保存し、転送、リモート接続は、共通であり、ネットワーク トラフィックが高い環境で重要な機能と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="fd278-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="fd278-109">MAPI スプーラーは、Outlook 内でバック グラウンド スレッドとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="fd278-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="fd278-110">MAPI スプーラーは、メッセージの配布に関連するその他の責任を持っています。</span><span class="sxs-lookup"><span data-stu-id="fd278-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="fd278-111">これらの余分な作業を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="fd278-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="fd278-112">追跡は、特定のトランスポート プロバイダーによって処理される受信者の種類です。</span><span class="sxs-lookup"><span data-stu-id="fd278-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="fd278-113">新しいメッセージが配信されたときにクライアント アプリケーションに通知します。</span><span class="sxs-lookup"><span data-stu-id="fd278-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="fd278-114">前処理スクリプトと後処理の呼び出しのメッセージです。</span><span class="sxs-lookup"><span data-stu-id="fd278-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="fd278-115">そのメッセージの配信を示すレポートを生成するが発生しました。</span><span class="sxs-lookup"><span data-stu-id="fd278-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="fd278-116">処理された受信者の状態を維持します。</span><span class="sxs-lookup"><span data-stu-id="fd278-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="fd278-117">次の図は、クライアントからのメッセージング システムにメッセージのフローを高レベルでは。</span><span class="sxs-lookup"><span data-stu-id="fd278-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="fd278-118">**出力メッセージ フロー**</span><span class="sxs-lookup"><span data-stu-id="fd278-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="fd278-119">![メッセージ フローの送信](media/amapi_46.gif "メッセージ フローの送信")</span><span class="sxs-lookup"><span data-stu-id="fd278-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="fd278-120">クライアント アプリケーションのユーザーは、1 つまたは複数の受信者にメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="fd278-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="fd278-121">メッセージは、送信側のプロセスでは、伝送のために必要な追加情報を持つメッセージの書式設定プロバイダーが初期化を格納します。</span><span class="sxs-lookup"><span data-stu-id="fd278-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="fd278-122">MAPI スプーラーは、次の条件のいずれかが発生した場合を処理するメッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="fd278-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="fd278-123">メッセージ ストア プロバイダーは、トランスポート プロバイダーの密結合されていません。</span><span class="sxs-lookup"><span data-stu-id="fd278-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="fd278-124">メッセージには、前処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="fd278-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="fd278-125">トランスポート、メッセージ ストア プロバイダーは緊密に結びついているが、相手にメッセージの宛先がすべての受信者を処理することはできません。</span><span class="sxs-lookup"><span data-stu-id="fd278-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="fd278-126">MAPI スプーラーは、メッセージを受信する必要な処理を実行し、適切なトランスポート プロバイダーにメッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="fd278-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="fd278-127">トランスポート プロバイダーは、そのメッセージング システム、その目的の受信者に送信するメッセージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fd278-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="fd278-128">受信メッセージの流れが逆になります。</span><span class="sxs-lookup"><span data-stu-id="fd278-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="fd278-129">トランスポート プロバイダーは、そのメッセージング システムからメッセージを受信し、MAPI スプーラーを通知します。</span><span class="sxs-lookup"><span data-stu-id="fd278-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="fd278-130">スプーラーでは、すべての必要な後処理を実行およびメッセージ ストア プロバイダーに新しいメッセージが到着したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="fd278-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="fd278-131">この通知には、新しいメッセージを確認するユーザーを有効にすると、メッセージの表示を更新するのにはクライアントが発生します。</span><span class="sxs-lookup"><span data-stu-id="fd278-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fd278-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd278-132">See also</span></span>

- [<span data-ttu-id="fd278-133">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="fd278-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

