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
# <a name="transport-provider-role-in-the-mapi-subsystem"></a><span data-ttu-id="00c49-103">MAPI サブシステムでのトランスポート プロバイダーの役割</span><span class="sxs-lookup"><span data-stu-id="00c49-103">Transport provider role in the MAPI subsystem</span></span>
  
<span data-ttu-id="00c49-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00c49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00c49-105">トランスポートプロバイダーのダイナミックリンクライブラリ (dll) は、MAPI スプーラーと、メッセージの送受信を行うメッセージングシステムの一部との間のインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="00c49-105">Transport provider dynamic-link libraries (DLLs) provide the interface between the MAPI spooler and the part of a messaging system responsible for message sending and receiving.</span></span> <span data-ttu-id="00c49-106">MAPI スプーラーとトランスポートプロバイダーが連携して、メッセージの送信またはメッセージの受信の責任を担います。</span><span class="sxs-lookup"><span data-stu-id="00c49-106">The MAPI spooler and the transport provider work together to handle the responsibilities of sending a message or receiving a message.</span></span> <span data-ttu-id="00c49-107">MAPI スプーラーは、トランスポートプロバイダー DLL が最初に使用されたときに読み込まれ、不要になった時点で解放されます。</span><span class="sxs-lookup"><span data-stu-id="00c49-107">The MAPI spooler loads the transport provider DLL when it is first used and releases it when it is no longer needed.</span></span> <span data-ttu-id="00c49-108">複数のトランスポートプロバイダーを同じシステムにインストールすることはできますが、MAPI は必要な1つのスプーラーを提供します。</span><span class="sxs-lookup"><span data-stu-id="00c49-108">Multiple transport providers can be installed on the same system, but MAPI supplies the one spooler required.</span></span>
  
<span data-ttu-id="00c49-109">クライアントアプリケーションは、通常、トランスポートプロバイダーと直接通信しません。</span><span class="sxs-lookup"><span data-stu-id="00c49-109">Client applications do not typically communicate directly with the transport provider.</span></span> <span data-ttu-id="00c49-110">代わりに、クライアントはストアプロバイダーを経由してメッセージを送信し、MAPI スプーラーは適切なトランスポートプロバイダーに送信メッセージを送信し、受信メッセージを適切なメッセージストアに配信します。</span><span class="sxs-lookup"><span data-stu-id="00c49-110">Rather, clients submit messages through a store provider and the MAPI spooler sends outgoing messages to the appropriate transport provider and delivers incoming messages to the appropriate message store.</span></span> <span data-ttu-id="00c49-111">フォアグラウンドアプリケーションがアイドル状態のときに MAPI スプーラーは動作を行い、トランスポートプロバイダーに呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="00c49-111">The MAPI spooler does its work and makes its calls to transport providers when foreground applications are idle.</span></span> <span data-ttu-id="00c49-112">トランスポートプロバイダーが最初にログオンしたときに、必要に応じてダイアログボックスを表示すると、トランスポートプロバイダーは、送信キューと受信キューをフラッシュするためにクライアントによって呼び出されない限り、バックグラウンドで動作します。</span><span class="sxs-lookup"><span data-stu-id="00c49-112">After optionally displaying dialog boxes when the transport provider is first logged on, transport providers operate in the background unless called by the client to flush send and receive queues.</span></span> 
  
<span data-ttu-id="00c49-113">トランスポートプロバイダーには、MAPI メッセージングシステムで次のような責任があります。</span><span class="sxs-lookup"><span data-stu-id="00c49-113">Transport providers have the following responsibilities in a MAPI messaging system:</span></span>
  
- <span data-ttu-id="00c49-114">mapi スプーラーで受け入れることができるアドレスの種類を登録します。これにより、mapi スプーラーは、メッセージの宛先アドレスに応じて、適切なトランスポートプロバイダーにメッセージを送信できます。</span><span class="sxs-lookup"><span data-stu-id="00c49-114">Register the address types they can accept with the MAPI spooler so the MAPI spooler can submit messages to the appropriate transport provider depending on the destination address of the messages.</span></span> <span data-ttu-id="00c49-115">1つのトランスポートプロバイダーは複数のアドレスの種類を登録できます。</span><span class="sxs-lookup"><span data-stu-id="00c49-115">One transport provider can register more than one address type.</span></span> <span data-ttu-id="00c49-116">また、トランスポートプロバイダーは、MAPI スプーラーで特定の受信者のアドレスを登録することもできます。</span><span class="sxs-lookup"><span data-stu-id="00c49-116">Transport providers can also register specific recipients' addresses with the MAPI spooler.</span></span> <span data-ttu-id="00c49-117">これらのアドレスのいずれかに宛てたメッセージは、MAPI スプーラーにアドレスを登録したトランスポートプロバイダーに送信されます。</span><span class="sxs-lookup"><span data-stu-id="00c49-117">Messages addressed to one of these addresses will be submitted to the transport provider that registered the address with the MAPI spooler.</span></span> <span data-ttu-id="00c49-118">詳細については、「 [Transport Provider and MAPI Spooler 操作モデル](transport-provider-and-mapi-spooler-operational-model.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00c49-118">For more information, see [Transport Provider and MAPI Spooler Operational Model](transport-provider-and-mapi-spooler-operational-model.md).</span></span>
    
- <span data-ttu-id="00c49-119">受信メッセージを MAPI スプーラーに配信します。</span><span class="sxs-lookup"><span data-stu-id="00c49-119">Deliver incoming messages to the MAPI spooler.</span></span> <span data-ttu-id="00c49-120">メッセージングシステムの性質に応じて、トランスポートプロバイダーは新しいメッセージが到着したときに mapi スプーラーに直接通知するか、または mapi スプーラーがトランスポートプロバイダーを定期的にポーリングして新しいメッセージをチェックするように要求することができます。</span><span class="sxs-lookup"><span data-stu-id="00c49-120">Depending on the nature of the messaging system, a transport provider can either directly notify the MAPI spooler when a new message arrives, or it can request that the MAPI spooler poll the transport provider periodically to check for new messages.</span></span>
    
- <span data-ttu-id="00c49-121">MAPI メッセージのプロパティを、メッセージングシステムにネイティブなメッセージプロパティとの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="00c49-121">Convert MAPI message properties to and from message properties native to the messaging system.</span></span> <span data-ttu-id="00c49-122">たとえば、トランスポートプロバイダーは、送信メッセージの送信者と受信者のアドレスを、メッセージングシステムで使用可能なフォームに変換する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="00c49-122">For example, the transport provider might have to convert the sender's and recipient's addresses in an outgoing message to a form that is acceptable to the messaging system.</span></span> <span data-ttu-id="00c49-123">一部のメッセージングシステムでは、すべての MAPI メッセージプロパティをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="00c49-123">Some messaging systems do not support all of the MAPI message properties.</span></span> <span data-ttu-id="00c49-124">メッセージングシステムにメッセージを配信するときの MAPI メッセージプロパティの保持の詳細については、「 [TNEF 対応のトランスポートプロバイダーを開発](developing-a-tnef-enabled-transport-provider.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00c49-124">For more information about preserving MAPI message properties when delivering messages to a messaging system, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
    
- <span data-ttu-id="00c49-125">トランスポートプロバイダーに固有のメッセージおよび受信者オプションを登録します。</span><span class="sxs-lookup"><span data-stu-id="00c49-125">Register message and recipient options specific to the transport provider.</span></span>
    
- <span data-ttu-id="00c49-126">メッセージングシステムに必要な資格情報の確認を行います。</span><span class="sxs-lookup"><span data-stu-id="00c49-126">Perform any verification of credentials required by the messaging system.</span></span>
    
- <span data-ttu-id="00c49-127">MAPI スプーラーによって渡された message オブジェクトを使用して、送信メッセージにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="00c49-127">Access outbound messages using the message object passed to it by the MAPI spooler.</span></span>
    
- <span data-ttu-id="00c49-128">基になるメッセージングシステムの必要に応じて、メッセージ形式を変換します。</span><span class="sxs-lookup"><span data-stu-id="00c49-128">Translate message format as required by the underlying messaging system.</span></span>
    
- <span data-ttu-id="00c49-129">[MAPI スプーラーに通知する] トランスポートプロバイダーが、その受信者の**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを設定することにより、処理の責務を負っている送信メッセージの受信者を通知します。</span><span class="sxs-lookup"><span data-stu-id="00c49-129">Notify the MAPI spooler which recipients of an outgoing message the transport provider has accepted responsibility for handling by setting the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for those recipients.</span></span>
    
- <span data-ttu-id="00c49-130">受信メッセージを処理する必要がある場合は、MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="00c49-130">Inform the MAPI spooler when an incoming message needs to be handled.</span></span>
    
- <span data-ttu-id="00c49-131">メッセージオブジェクトを使用して、受信メッセージデータを MAPI スプーラーに渡します。</span><span class="sxs-lookup"><span data-stu-id="00c49-131">Pass incoming message data to the MAPI spooler by using message objects.</span></span>
    
- <span data-ttu-id="00c49-132">受信メッセージのすべての必要な MAPI メッセージプロパティに値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="00c49-132">Assign values to all required MAPI message properties on incoming messages.</span></span>
    
- <span data-ttu-id="00c49-133">必要に応じて、配信後に基になるメッセージングシステムからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="00c49-133">Delete the message from the underlying messaging system after delivery, if necessary.</span></span>
    
- <span data-ttu-id="00c49-134">MAPI スプーラーおよびクライアントアプリケーションの状態情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="00c49-134">Provide status information for the MAPI spooler and client applications.</span></span>
    
<span data-ttu-id="00c49-135">次の図は、MAPI アーキテクチャの他のコンポーネントに対するトランスポートプロバイダーの役割を示しています。</span><span class="sxs-lookup"><span data-stu-id="00c49-135">The following illustration shows a transport provider's role with respect to the other components of the MAPI architecture.</span></span>
  
<span data-ttu-id="00c49-136">**メッセージング システムのトランスポート プロバイダー ロール**</span><span class="sxs-lookup"><span data-stu-id="00c49-136">**Transport provider role in a messaging system**</span></span>
  
<span data-ttu-id="00c49-137">![メッセージングシステムでのトランスポートプロバイダーの役割](media/xp01.gif "メッセージングシステムでのトランスポートプロバイダーの役割")</span><span class="sxs-lookup"><span data-stu-id="00c49-137">![Transport provider role in a messaging system](media/xp01.gif "Transport provider role in a messaging system")</span></span>
  

