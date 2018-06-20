---
title: MAPI のサブシステムのトランスポート プロバイダーの役割
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7659369a-0952-4f5a-a86b-91958c4c1a3f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7ea60b73fb1abe32b6db5e3c73d6ef3fac53d35d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804131"
---
# <a name="transport-provider-role-in-the-mapi-subsystem"></a><span data-ttu-id="d52ce-103">MAPI のサブシステムのトランスポート プロバイダーの役割</span><span class="sxs-lookup"><span data-stu-id="d52ce-103">Transport provider role in the MAPI subsystem</span></span>
  
<span data-ttu-id="d52ce-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d52ce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d52ce-105">トランスポート プロバイダーのダイナミック リンク ライブラリ (Dll) では、MAPI スプーラーとメッセージの送信と受信を担当するメッセージング システムの部品間のインタ フェースを提供します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-105">Transport provider dynamic-link libraries (DLLs) provide the interface between the MAPI spooler and the part of a messaging system responsible for message sending and receiving.</span></span> <span data-ttu-id="d52ce-106">MAPI スプーラーとトランスポート プロバイダーは、メッセージの送信や受信メッセージの責任を処理するために連携します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-106">The MAPI spooler and the transport provider work together to handle the responsibilities of sending a message or receiving a message.</span></span> <span data-ttu-id="d52ce-107">MAPI スプーラーは、最初に使用されるし、不要になった時に解放する場合に、トランスポート プロバイダーの DLL を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="d52ce-107">The MAPI spooler loads the transport provider DLL when it is first used and releases it when it is no longer needed.</span></span> <span data-ttu-id="d52ce-108">同じシステムに複数のトランスポート プロバイダーをインストールすることができますが、MAPI が必要な 1 つのスプーラーを提供します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-108">Multiple transport providers can be installed on the same system, but MAPI supplies the one spooler required.</span></span>
  
<span data-ttu-id="d52ce-109">クライアント アプリケーションは、通常はトランスポート プロバイダーと直接通信しません。</span><span class="sxs-lookup"><span data-stu-id="d52ce-109">Client applications do not typically communicate directly with the transport provider.</span></span> <span data-ttu-id="d52ce-110">代わりに、クライアントは、ストア プロバイダーを経由してメッセージを送信し、MAPI スプーラーが適切なトランスポート プロバイダーに送信するメッセージを送信し、適切なメッセージ ・ ストアに受信メッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-110">Rather, clients submit messages through a store provider and the MAPI spooler sends outgoing messages to the appropriate transport provider and delivers incoming messages to the appropriate message store.</span></span> <span data-ttu-id="d52ce-111">MAPI スプーラー機能の動作し、フォア グラウンド アプリケーションがアイドル状態のときに、プロバイダーをトランスポートするための呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="d52ce-111">The MAPI spooler does its work and makes its calls to transport providers when foreground applications are idle.</span></span> <span data-ttu-id="d52ce-112">トランスポート プロバイダーが最初に必要に応じてダイアログ ボックスを表示するがログオンした後、トランスポート プロバイダーは、送信および受信キューをフラッシュするにクライアントによって呼び出される場合を除き、バック グラウンドで動作します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-112">After optionally displaying dialog boxes when the transport provider is first logged on, transport providers operate in the background unless called by the client to flush send and receive queues.</span></span> 
  
<span data-ttu-id="d52ce-113">トランスポート プロバイダーでは、MAPI メッセージング システムに次の責任があります。</span><span class="sxs-lookup"><span data-stu-id="d52ce-113">Transport providers have the following responsibilities in a MAPI messaging system:</span></span>
  
- <span data-ttu-id="d52ce-114">MAPI スプーラーは、適切なトランスポート プロバイダーによっては、メッセージの宛先アドレスにメッセージを送信できるように、MAPI スプーラーを無効に使用できるアドレスの種類を登録します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-114">Register the address types they can accept with the MAPI spooler so the MAPI spooler can submit messages to the appropriate transport provider depending on the destination address of the messages.</span></span> <span data-ttu-id="d52ce-115">1 つのトランスポート プロバイダーは、複数のアドレスの種類を登録できます。</span><span class="sxs-lookup"><span data-stu-id="d52ce-115">One transport provider can register more than one address type.</span></span> <span data-ttu-id="d52ce-116">トランスポート プロバイダーは、MAPI スプーラーを無効に特定の受信者のアドレスを登録することもできます。</span><span class="sxs-lookup"><span data-stu-id="d52ce-116">Transport providers can also register specific recipients' addresses with the MAPI spooler.</span></span> <span data-ttu-id="d52ce-117">これらのアドレスのいずれかに送信されるメッセージは、MAPI スプーラーにアドレスを登録されているトランスポート プロバイダーに送信されます。</span><span class="sxs-lookup"><span data-stu-id="d52ce-117">Messages addressed to one of these addresses will be submitted to the transport provider that registered the address with the MAPI spooler.</span></span> <span data-ttu-id="d52ce-118">詳細については、[トランスポート プロバイダーおよび MAPI スプーラーの運用モデル](transport-provider-and-mapi-spooler-operational-model.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d52ce-118">For more information, see [Transport Provider and MAPI Spooler Operational Model](transport-provider-and-mapi-spooler-operational-model.md).</span></span>
    
- <span data-ttu-id="d52ce-119">MAPI スプーラーを無効にするには、受信メッセージを提供します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-119">Deliver incoming messages to the MAPI spooler.</span></span> <span data-ttu-id="d52ce-120">メッセージング システムによっては、トランスポート プロバイダーことができますか、直接 MAPI スプーラーを無効またはときに通知、新しいメッセージが到着すると、MAPI スプーラーにトランスポート プロバイダーは、新しいメッセージをチェックするには、定期的にポーリングを要求することができます。</span><span class="sxs-lookup"><span data-stu-id="d52ce-120">Depending on the nature of the messaging system, a transport provider can either directly notify the MAPI spooler when a new message arrives, or it can request that the MAPI spooler poll the transport provider periodically to check for new messages.</span></span>
    
- <span data-ttu-id="d52ce-121">間のメッセージング システムとネイティブ ・ メッセージ ・ プロパティは、MAPI メッセージのプロパティを変換します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-121">Convert MAPI message properties to and from message properties native to the messaging system.</span></span> <span data-ttu-id="d52ce-122">などのトランスポート プロバイダーは、メッセージング システムに許容されるフォームを送信メッセージに、送信者と受信者のアドレスを変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d52ce-122">For example, the transport provider might have to convert the sender's and recipient's addresses in an outgoing message to a form that is acceptable to the messaging system.</span></span> <span data-ttu-id="d52ce-123">いくつかのメッセージング システムはすべての MAPI メッセージのプロパティはサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="d52ce-123">Some messaging systems do not support all of the MAPI message properties.</span></span> <span data-ttu-id="d52ce-124">メッセージング システムにメッセージを配信する場合は、MAPI メッセージのプロパティを保存する方法についての詳細については、 [TNEF-Enabled トランスポート プロバイダーの開発](developing-a-tnef-enabled-transport-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d52ce-124">For more information about preserving MAPI message properties when delivering messages to a messaging system, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
    
- <span data-ttu-id="d52ce-125">トランスポート プロバイダーに固有のメッセージと受信者のオプションを登録します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-125">Register message and recipient options specific to the transport provider.</span></span>
    
- <span data-ttu-id="d52ce-126">メッセージング システムに必要な資格情報の確認を実行します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-126">Perform any verification of credentials required by the messaging system.</span></span>
    
- <span data-ttu-id="d52ce-127">メッセージ オブジェクトを使用して送信メッセージにアクセスは、MAPI スプーラーによってに渡されます。</span><span class="sxs-lookup"><span data-stu-id="d52ce-127">Access outbound messages using the message object passed to it by the MAPI spooler.</span></span>
    
- <span data-ttu-id="d52ce-128">基になるメッセージング システムで必要なメッセージ形式を変換します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-128">Translate message format as required by the underlying messaging system.</span></span>
    
- <span data-ttu-id="d52ce-129">MAPI スプーラーを無効にする受信者の**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) のプロパティを設定することによって処理のための責任を受け入れたトランスポート プロバイダーは、送信メッセージの受信者を通知します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-129">Notify the MAPI spooler which recipients of an outgoing message the transport provider has accepted responsibility for handling by setting the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for those recipients.</span></span>
    
- <span data-ttu-id="d52ce-130">MAPI スプーラーは、受信メッセージを処理する必要があるときに通知します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-130">Inform the MAPI spooler when an incoming message needs to be handled.</span></span>
    
- <span data-ttu-id="d52ce-131">メッセージ オブジェクトを使用して、MAPI スプーラーを無効に受信メッセージのデータを渡します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-131">Pass incoming message data to the MAPI spooler by using message objects.</span></span>
    
- <span data-ttu-id="d52ce-132">受信メッセージに必要な MAPI メッセージ プロパティをすべてに値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d52ce-132">Assign values to all required MAPI message properties on incoming messages.</span></span>
    
- <span data-ttu-id="d52ce-133">必要な場合に、配信後、基になるメッセージング システムからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-133">Delete the message from the underlying messaging system after delivery, if necessary.</span></span>
    
- <span data-ttu-id="d52ce-134">MAPI スプーラーとクライアント アプリケーションの状態に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-134">Provide status information for the MAPI spooler and client applications.</span></span>
    
<span data-ttu-id="d52ce-135">MAPI アーキテクチャの他のコンポーネントについて、トランスポート プロバイダーの役割を次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="d52ce-135">The following illustration shows a transport provider's role with respect to the other components of the MAPI architecture.</span></span>
  
<span data-ttu-id="d52ce-136">**メッセージング システムでトランスポート プロバイダーの役割**</span><span class="sxs-lookup"><span data-stu-id="d52ce-136">**Transport provider role in a messaging system**</span></span>
  
<span data-ttu-id="d52ce-137">![メッセージング システムでトランスポート プロバイダーの役割](media/xp01.gif "メッセージング システムでトランスポート プロバイダーの役割")</span><span class="sxs-lookup"><span data-stu-id="d52ce-137">![Transport provider role in a messaging system](media/xp01.gif "Transport provider role in a messaging system")</span></span>
  

