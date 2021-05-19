---
title: MAPI クライアント アプリケーションの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410036"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="62fee-103">MAPI クライアント アプリケーションの開発</span><span class="sxs-lookup"><span data-stu-id="62fee-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="62fee-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62fee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62fee-105">MAPI クライアント アプリケーションは、オブジェクト指向の MAPI クライアント インターフェイスを使用して書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="62fee-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="62fee-106">MAPI クライアントは、MAPI サブシステムと MAPI 準拠のサービス プロバイダーを介して 1 つ以上のメッセージング システムと対話します。</span><span class="sxs-lookup"><span data-stu-id="62fee-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="62fee-107">この相互作用は、さまざまな方法で発生する可能性があります。クライアント アプリケーションには非常に多様な機能があります。</span><span class="sxs-lookup"><span data-stu-id="62fee-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="62fee-108">ほとんどのクライアントはメッセージング クライアントで、メッセージングを確立された機能セットに統合するか、メッセージングを主な機能として実行します。</span><span class="sxs-lookup"><span data-stu-id="62fee-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="62fee-109">MAPI クライアントが提供するその他の機能には、プロファイル管理またはアドレス帳とメッセージ ストアの管理があります。</span><span class="sxs-lookup"><span data-stu-id="62fee-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="62fee-110">すべてのメッセージング クライアントが MAPI ライブラリを初期化し、MAPI **サブシステムとの** セッションを開始します。</span><span class="sxs-lookup"><span data-stu-id="62fee-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="62fee-111">詳細については、「セッションを [使用してオブジェクトにアクセスする」を参照してください](accessing-objects-by-using-the-session.md)。</span><span class="sxs-lookup"><span data-stu-id="62fee-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="62fee-112">セッションが確立されると、クライアントは次の機能を実行できます。</span><span class="sxs-lookup"><span data-stu-id="62fee-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="62fee-113">返信、転送メッセージ、再送信などの送信メッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="62fee-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="62fee-114">受信メッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="62fee-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="62fee-115">フォルダーとメッセージを開き、メッセージの作成、変更、コピー、送信、会話の追跡、1 つ以上のフォルダーの検索を行って、メッセージ ストアを処理します。</span><span class="sxs-lookup"><span data-stu-id="62fee-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="62fee-116">受信者の作成と変更、エントリの検索、コンテナー階層の移動によってアドレス帳を処理します。</span><span class="sxs-lookup"><span data-stu-id="62fee-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="62fee-117">再構成を実行し、オプションとトランスポートの順序を設定し、オンデマンドでメッセージを送信することで、トランスポート プロバイダーを処理します。</span><span class="sxs-lookup"><span data-stu-id="62fee-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="62fee-118">イベント通知を処理します。</span><span class="sxs-lookup"><span data-stu-id="62fee-118">Handle event notification.</span></span>
    
- <span data-ttu-id="62fee-119">フォームを処理します。</span><span class="sxs-lookup"><span data-stu-id="62fee-119">Handle forms.</span></span>
    
- <span data-ttu-id="62fee-120">プロファイルとメッセージ サービスを処理します。</span><span class="sxs-lookup"><span data-stu-id="62fee-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="62fee-121">このセクションのトピックを使用して、これらの基本的なタスクと MAPI クライアントを一意にする特定の機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="62fee-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

