---
title: MAPI クライアント アプリケーションを開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 42558fcc3d94b108c0dabb92d62f7c61fdf3039f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799912"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="5c607-103">MAPI クライアント アプリケーションを開発</span><span class="sxs-lookup"><span data-stu-id="5c607-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="5c607-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5c607-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5c607-105">MAPI クライアント アプリケーションは、オブジェクト指向の MAPI クライアント インターフェイスを使用して書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="5c607-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="5c607-106">MAPI クライアントは、MAPI のサブシステムと MAPI 準拠のサービス プロバイダーを 1 つまたは複数のメッセージング システムと対話します。</span><span class="sxs-lookup"><span data-stu-id="5c607-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="5c607-107">この相互作用は、多くの異なる方法で発生する可能性クライアント アプリケーションで、膨大な種類があります。</span><span class="sxs-lookup"><span data-stu-id="5c607-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="5c607-108">ほとんどのクライアントは、クライアントでは、メッセージング、確立された機能セットをまたはメッセージングの主要な機能として実行することを統合するかをメッセージは。</span><span class="sxs-lookup"><span data-stu-id="5c607-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="5c607-109">MAPI クライアントが提供するその他の機能は、プロファイルの管理やアドレス帳とメッセージ ・ ストアの管理。</span><span class="sxs-lookup"><span data-stu-id="5c607-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="5c607-110">すべてのメッセージング クライアントは、MAPI ライブラリを初期化し、MAPI のサブシステムと**のセッション**を開始します。</span><span class="sxs-lookup"><span data-stu-id="5c607-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="5c607-111">詳細については、[セッションを使用して、オブジェクトへのアクセス](accessing-objects-by-using-the-session.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c607-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="5c607-112">セッションが確立されると、クライアントを実行できます。</span><span class="sxs-lookup"><span data-stu-id="5c607-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="5c607-113">返信、転送、メッセージ、および再送信を含む送信メッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="5c607-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="5c607-114">受信メッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="5c607-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="5c607-115">開く, フォルダーとメッセージを作成、変更、コピー、およびメッセージを送信する、会話を追跡、および 1 つまたは複数のフォルダーを検索してメッセージ ・ ストアを処理します。</span><span class="sxs-lookup"><span data-stu-id="5c607-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="5c607-116">作成して、受信者を変更する、エントリを検索するコンテナーの階層を走査するには、アドレス帳を処理します。</span><span class="sxs-lookup"><span data-stu-id="5c607-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="5c607-117">再構成を実行するし、オプションとトランスポートの順番を設定し、要求時にメッセージを送信するには、トランスポート プロバイダーを処理します。</span><span class="sxs-lookup"><span data-stu-id="5c607-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="5c607-118">イベント通知を処理します。</span><span class="sxs-lookup"><span data-stu-id="5c607-118">Handle event notification.</span></span>
    
- <span data-ttu-id="5c607-119">フォームを処理します。</span><span class="sxs-lookup"><span data-stu-id="5c607-119">Handle forms.</span></span>
    
- <span data-ttu-id="5c607-120">プロファイルとメッセージ サービスを処理します。</span><span class="sxs-lookup"><span data-stu-id="5c607-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="5c607-121">これらの基本的なタスクと、MAPI クライアントを一意にする、特定の機能を実装するため、このセクションのトピックを使用します。</span><span class="sxs-lookup"><span data-stu-id="5c607-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

