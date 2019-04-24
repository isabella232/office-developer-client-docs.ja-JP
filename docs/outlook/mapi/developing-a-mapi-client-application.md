---
title: MAPI クライアントアプリケーションの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316689"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="985fd-103">MAPI クライアントアプリケーションの開発</span><span class="sxs-lookup"><span data-stu-id="985fd-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="985fd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="985fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="985fd-105">mapi クライアントアプリケーションは、オブジェクト指向の mapi クライアントインターフェイスを使用して記述されます。</span><span class="sxs-lookup"><span data-stu-id="985fd-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="985fd-106">mapi クライアントは、mapi サブシステムと mapi 準拠のサービスプロバイダーを使用して、1つまたは複数のメッセージングシステムと対話します。</span><span class="sxs-lookup"><span data-stu-id="985fd-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="985fd-107">この操作はさまざまな方法で行われることがあります。クライアントアプリケーションにはさまざまな種類があります。</span><span class="sxs-lookup"><span data-stu-id="985fd-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="985fd-108">ほとんどのクライアントはメッセージングクライアントであり、メッセージングを確立された機能セットに統合するか、または主要な機能としてメッセージングを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="985fd-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="985fd-109">MAPI クライアントが提供するその他の機能には、プロファイル管理、アドレス帳、およびメッセージストア管理があります。</span><span class="sxs-lookup"><span data-stu-id="985fd-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="985fd-110">すべてのメッセージングクライアントは mapi ライブラリを初期化し、mapi サブシステムを使用して**セッション**を開始します。</span><span class="sxs-lookup"><span data-stu-id="985fd-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="985fd-111">詳細については、「 [Session を使用してオブジェクトにアクセス](accessing-objects-by-using-the-session.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="985fd-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="985fd-112">セッションが確立されると、クライアントは次のことを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="985fd-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="985fd-113">返信、転送されたメッセージ、再送などの送信メッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="985fd-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="985fd-114">受信メッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="985fd-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="985fd-115">フォルダーとメッセージを開く、メッセージの作成、変更、コピー、および送信、会話の追跡、1つまたは複数のフォルダーの検索を行って、メッセージストアを処理します。</span><span class="sxs-lookup"><span data-stu-id="985fd-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="985fd-116">受信者の作成と変更、エントリの検索、およびコンテナー階層の走査を行って、アドレス帳を処理します。</span><span class="sxs-lookup"><span data-stu-id="985fd-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="985fd-117">再構成を実行し、オプションとトランスポート順序を設定し、必要に応じてメッセージを送信して、トランスポートプロバイダーを処理します。</span><span class="sxs-lookup"><span data-stu-id="985fd-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="985fd-118">イベント通知を処理します。</span><span class="sxs-lookup"><span data-stu-id="985fd-118">Handle event notification.</span></span>
    
- <span data-ttu-id="985fd-119">フォームを処理します。</span><span class="sxs-lookup"><span data-stu-id="985fd-119">Handle forms.</span></span>
    
- <span data-ttu-id="985fd-120">プロファイルとメッセージサービスを処理します。</span><span class="sxs-lookup"><span data-stu-id="985fd-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="985fd-121">このセクションのトピックを使用して、これらの基本的なタスクと、MAPI クライアントを一意にするための特定の機能を実装するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="985fd-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

