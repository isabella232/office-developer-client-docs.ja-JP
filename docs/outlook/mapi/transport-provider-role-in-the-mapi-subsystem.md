---
title: MAPI サブシステムでのトランスポート プロバイダーの役割
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7cadb57706e3feec7ed98dd5e4e8d75967036fef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424057"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a><span data-ttu-id="4d78f-103">MAPI サブシステムでのトランスポート プロバイダーの役割</span><span class="sxs-lookup"><span data-stu-id="4d78f-103">Transport provider role in the MAPI subsystem</span></span>
  
<span data-ttu-id="4d78f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d78f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d78f-105">トランスポート プロバイダーの動的リンク ライブラリ (DLL) は、MAPI スプーラーとメッセージの送受信を担当するメッセージング システムの一部との間のインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-105">Transport provider dynamic-link libraries (DLLs) provide the interface between the MAPI spooler and the part of a messaging system responsible for message sending and receiving.</span></span> <span data-ttu-id="4d78f-106">MAPI スプーラーとトランスポート プロバイダーは、メッセージの送信またはメッセージの受信の責任を処理するために一緒に作業します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-106">The MAPI spooler and the transport provider work together to handle the responsibilities of sending a message or receiving a message.</span></span> <span data-ttu-id="4d78f-107">MAPI スプーラーは、トランスポート プロバイダー DLL を最初に使用するときに読み込み、不要になったときに解放します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-107">The MAPI spooler loads the transport provider DLL when it is first used and releases it when it is no longer needed.</span></span> <span data-ttu-id="4d78f-108">複数のトランスポート プロバイダーを同じシステムにインストールできますが、MAPI は必要なスプーラーを 1 つ提供します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-108">Multiple transport providers can be installed on the same system, but MAPI supplies the one spooler required.</span></span>
  
<span data-ttu-id="4d78f-109">通常、クライアント アプリケーションはトランスポート プロバイダーと直接通信しない。</span><span class="sxs-lookup"><span data-stu-id="4d78f-109">Client applications do not typically communicate directly with the transport provider.</span></span> <span data-ttu-id="4d78f-110">クライアントはストア プロバイダーを介してメッセージを送信し、MAPI スプーラーは送信メッセージを適切なトランスポート プロバイダーに送信し、受信メッセージを適切なメッセージ ストアに配信します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-110">Rather, clients submit messages through a store provider and the MAPI spooler sends outgoing messages to the appropriate transport provider and delivers incoming messages to the appropriate message store.</span></span> <span data-ttu-id="4d78f-111">MAPI スプーラーは、その作業を実行し、フォアグラウンド アプリケーションがアイドル状態のときにトランスポート プロバイダーへの呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="4d78f-111">The MAPI spooler does its work and makes its calls to transport providers when foreground applications are idle.</span></span> <span data-ttu-id="4d78f-112">必要に応じて、トランスポート プロバイダーが最初にログオンするときにダイアログ ボックスを表示した後、送信キューと受信キューをフラッシュするためにクライアントから呼び出されない限り、トランスポート プロバイダーはバックグラウンドで動作します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-112">After optionally displaying dialog boxes when the transport provider is first logged on, transport providers operate in the background unless called by the client to flush send and receive queues.</span></span> 
  
<span data-ttu-id="4d78f-113">トランスポート プロバイダーは、MAPI メッセージング システムで次の責任を負います。</span><span class="sxs-lookup"><span data-stu-id="4d78f-113">Transport providers have the following responsibilities in a MAPI messaging system:</span></span>
  
- <span data-ttu-id="4d78f-114">MAPI スプーラーがメッセージの宛先アドレスに応じて適切なトランスポート プロバイダーにメッセージを送信できるよう、MAPI スプーラーで受け入れ可能なアドレスの種類を登録します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-114">Register the address types they can accept with the MAPI spooler so the MAPI spooler can submit messages to the appropriate transport provider depending on the destination address of the messages.</span></span> <span data-ttu-id="4d78f-115">1 つのトランスポート プロバイダーは、複数のアドレスの種類を登録できます。</span><span class="sxs-lookup"><span data-stu-id="4d78f-115">One transport provider can register more than one address type.</span></span> <span data-ttu-id="4d78f-116">トランスポート プロバイダーは、MAPI スプーラーに特定の受信者のアドレスを登録することもできます。</span><span class="sxs-lookup"><span data-stu-id="4d78f-116">Transport providers can also register specific recipients' addresses with the MAPI spooler.</span></span> <span data-ttu-id="4d78f-117">これらのアドレスの 1 つにアドレス指定されたメッセージは、MAPI スプーラーにアドレスを登録したトランスポート プロバイダーに送信されます。</span><span class="sxs-lookup"><span data-stu-id="4d78f-117">Messages addressed to one of these addresses will be submitted to the transport provider that registered the address with the MAPI spooler.</span></span> <span data-ttu-id="4d78f-118">詳細については、「トランスポート プロバイダー [と MAPI スプーラー運用モデル」を参照してください](transport-provider-and-mapi-spooler-operational-model.md)。</span><span class="sxs-lookup"><span data-stu-id="4d78f-118">For more information, see [Transport Provider and MAPI Spooler Operational Model](transport-provider-and-mapi-spooler-operational-model.md).</span></span>
    
- <span data-ttu-id="4d78f-119">MAPI スプーラーに受信メッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-119">Deliver incoming messages to the MAPI spooler.</span></span> <span data-ttu-id="4d78f-120">メッセージング システムの性質に応じて、トランスポート プロバイダーは、新しいメッセージが到着すると MAPI スプーラーに直接通知するか、MAPI スプーラーがトランスポート プロバイダーを定期的にポーリングして新しいメッセージを確認する要求を行います。</span><span class="sxs-lookup"><span data-stu-id="4d78f-120">Depending on the nature of the messaging system, a transport provider can either directly notify the MAPI spooler when a new message arrives, or it can request that the MAPI spooler poll the transport provider periodically to check for new messages.</span></span>
    
- <span data-ttu-id="4d78f-121">MAPI メッセージ のプロパティを、メッセージング システムにネイティブなメッセージ プロパティに変換します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-121">Convert MAPI message properties to and from message properties native to the messaging system.</span></span> <span data-ttu-id="4d78f-122">たとえば、トランスポート プロバイダーは、送信メッセージ内の送信者と受信者のアドレスを、メッセージング システムで受け入れられるフォームに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d78f-122">For example, the transport provider might have to convert the sender's and recipient's addresses in an outgoing message to a form that is acceptable to the messaging system.</span></span> <span data-ttu-id="4d78f-123">一部のメッセージング システムでは、すべての MAPI メッセージ プロパティがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4d78f-123">Some messaging systems do not support all of the MAPI message properties.</span></span> <span data-ttu-id="4d78f-124">メッセージング システムにメッセージを配信するときに MAPI メッセージのプロパティを保持する方法の詳細については、「メッセージ トランスポート プロバイダーの開発TNEF-Enabled [参照してください](developing-a-tnef-enabled-transport-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="4d78f-124">For more information about preserving MAPI message properties when delivering messages to a messaging system, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
    
- <span data-ttu-id="4d78f-125">トランスポート プロバイダーに固有のメッセージと受信者のオプションを登録します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-125">Register message and recipient options specific to the transport provider.</span></span>
    
- <span data-ttu-id="4d78f-126">メッセージング システムで必要な資格情報の検証を実行します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-126">Perform any verification of credentials required by the messaging system.</span></span>
    
- <span data-ttu-id="4d78f-127">MAPI スプーラーによって渡されたメッセージ オブジェクトを使用して、送信メッセージにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4d78f-127">Access outbound messages using the message object passed to it by the MAPI spooler.</span></span>
    
- <span data-ttu-id="4d78f-128">基になるメッセージング システムで必要に応じてメッセージ形式を変換します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-128">Translate message format as required by the underlying messaging system.</span></span>
    
- <span data-ttu-id="4d78f-129">これらの受信者の **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを設定して、トランスポート プロバイダーが処理の責任を受け入れる送信メッセージの受信者を MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-129">Notify the MAPI spooler which recipients of an outgoing message the transport provider has accepted responsibility for handling by setting the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for those recipients.</span></span>
    
- <span data-ttu-id="4d78f-130">受信メッセージを処理する必要がある場合は、MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-130">Inform the MAPI spooler when an incoming message needs to be handled.</span></span>
    
- <span data-ttu-id="4d78f-131">メッセージ オブジェクトを使用して、受信メッセージ データを MAPI スプーラーに渡します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-131">Pass incoming message data to the MAPI spooler by using message objects.</span></span>
    
- <span data-ttu-id="4d78f-132">受信メッセージに必要なすべての MAPI メッセージ プロパティに値を割り当てる。</span><span class="sxs-lookup"><span data-stu-id="4d78f-132">Assign values to all required MAPI message properties on incoming messages.</span></span>
    
- <span data-ttu-id="4d78f-133">必要に応じて、配信後に基になるメッセージング システムからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-133">Delete the message from the underlying messaging system after delivery, if necessary.</span></span>
    
- <span data-ttu-id="4d78f-134">MAPI スプーラーとクライアント アプリケーションの状態情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="4d78f-134">Provide status information for the MAPI spooler and client applications.</span></span>
    
<span data-ttu-id="4d78f-135">次の図は、MAPI アーキテクチャの他のコンポーネントに関するトランスポート プロバイダーの役割を示しています。</span><span class="sxs-lookup"><span data-stu-id="4d78f-135">The following illustration shows a transport provider's role with respect to the other components of the MAPI architecture.</span></span>
  
<span data-ttu-id="4d78f-136">**メッセージング システムのトランスポート プロバイダー ロール**</span><span class="sxs-lookup"><span data-stu-id="4d78f-136">**Transport provider role in a messaging system**</span></span>
  
<span data-ttu-id="4d78f-137">![メッセージング システムのトランスポート プロバイダーの役割]メッセージング システム(media/xp01.gif "内のトランスポート プロバイダーの役割")</span><span class="sxs-lookup"><span data-stu-id="4d78f-137">![Transport provider role in a messaging system](media/xp01.gif "Transport provider role in a messaging system")</span></span>
  

