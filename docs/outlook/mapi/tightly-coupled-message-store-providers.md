---
title: 密結合メッセージストアプロバイダー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3c9996dad1e9aa8c291f1cd593d9651994d86141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413228"
---
# <a name="tightly-coupled-message-store-providers"></a><span data-ttu-id="57e21-103">密結合メッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="57e21-103">Tightly Coupled Message Store Providers</span></span>

  
  
<span data-ttu-id="57e21-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57e21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57e21-105">メッセージストアプロバイダーは、トランスポートプロバイダーと密に結合できます。</span><span class="sxs-lookup"><span data-stu-id="57e21-105">Message store providers can be tightly coupled with a transport provider.</span></span> <span data-ttu-id="57e21-106">MAPI サービスプロバイダーは、ストアプロバイダーとトランスポートプロバイダーが通信できるように2つのプロバイダーを実装することによって、メッセージの送信と受信をより効率的に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="57e21-106">Tightly coupling MAPI service providers means implementing the two providers such that the store provider and transport provider can communicate to make the process of sending and receiving messages more efficient.</span></span> <span data-ttu-id="57e21-107">これを実現する利点は、2つのサービスプロバイダーが MAPI スプーラーを使用するのではなく、互いに直接対話できる場合に、パフォーマンスが向上する可能性があることです。</span><span class="sxs-lookup"><span data-stu-id="57e21-107">The benefit of doing this is that performance improvements can result when two service providers can interact with each other directly rather than by means of MAPI spooler.</span></span> <span data-ttu-id="57e21-108">メッセージストアプロバイダーを厳密にトランスポートプロバイダーに結合するには、トランスポートプロバイダーは、トランスポートプロバイダーの**PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) プロパティにメッセージストアプロバイダーのエントリ識別子を配置する必要があります。MAPI 状態テーブルの行。</span><span class="sxs-lookup"><span data-stu-id="57e21-108">To tightly couple a message store provider to a transport provider, the transport provider must place the message store provider's entry identifier in the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in the transport provider's row in the MAPI status table.</span></span> <span data-ttu-id="57e21-109">これにより、MAPI スプーラーはストアプロバイダーをトランスポートプロバイダーに接続できます。</span><span class="sxs-lookup"><span data-stu-id="57e21-109">This enables MAPI spooler to connect the store provider to the transport provider.</span></span>
  
<span data-ttu-id="57e21-110">メッセージストアプロバイダーを他のサービスプロバイダーと密に結合する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="57e21-110">There is no requirement that a message store provider ever be tightly coupled with any other service provider.</span></span> <span data-ttu-id="57e21-111">メッセージストアプロバイダーと密接に連携する最も一般的なサービスプロバイダーは、トランスポートプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="57e21-111">The most common service provider to tightly couple with a message store provider is a transport provider.</span></span> <span data-ttu-id="57e21-112">これは通常、MAPI スプーラーを使用せずに、メッセージの送受信を行うことができるようにするためです。</span><span class="sxs-lookup"><span data-stu-id="57e21-112">This is usually done so that sending and receiving messages can be accomplished without involving the MAPI spooler.</span></span> <span data-ttu-id="57e21-113">たとえば、ユーザーが送信メッセージを送信すると、メッセージストアプロバイダーとトランスポートプロバイダーの組み合わせによって直接送信できます。</span><span class="sxs-lookup"><span data-stu-id="57e21-113">For example, when the user submits an outgoing message, the combined message store provider and transport provider can send it directly.</span></span> <span data-ttu-id="57e21-114">統合されたサービスプロバイダーは、最初に処理すべき新しいメッセージがあることを mapi スプーラーに通知し、mapi スプーラーがメッセージストアプロバイダーからトランスポートプロバイダーにメッセージを転送するプロセスを開始するのを待機する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="57e21-114">The combined service providers do not have to first notify MAPI spooler that there is a new message to process and then wait for MAPI spooler to initiate the process of transferring the message from the message store provider to the transport provider.</span></span> <span data-ttu-id="57e21-115">これは、ユーザーのコンピューターとサーバー間のネットワークトラフィックを最小限に抑えることによって、サーバーベースのメッセージストアが使用されている場合に特に利点があります。</span><span class="sxs-lookup"><span data-stu-id="57e21-115">This has particular benefits when a server-based message store is being used by minimizing network traffic between the user's computer and the server.</span></span>
  
<span data-ttu-id="57e21-116">一般に、サービスプロバイダーを密に結合するための適切に指定された手順はありません。</span><span class="sxs-lookup"><span data-stu-id="57e21-116">In general, there are no well-specified procedures for tightly coupling service providers.</span></span> <span data-ttu-id="57e21-117">ただし、次のガイドラインを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57e21-117">However, you should use the following guidelines:</span></span>
  
- <span data-ttu-id="57e21-118">サービスプロバイダーが密に結合している理由がパフォーマンスにある場合は、これらのパーツが通常関与するプロセスから MAPI サブシステムの一部を取得することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="57e21-118">If the reason for tightly coupling service providers is performance, be aware that the coupling takes parts of the MAPI subsystem out of the processes that those parts would normally be involved in.</span></span> <span data-ttu-id="57e21-119">これは、統合されたサービスプロバイダーの個々のパーツが相互に通信する必要があることを意味します。これは、通常、使用されていない MAPI サブシステムの部分に対する対話をシミュレートすることです。</span><span class="sxs-lookup"><span data-stu-id="57e21-119">This implies that the individual parts in the combined service provider should interact with each other in a way that simulates the interaction they would normally have with the parts of the MAPI subsystem that are not being used.</span></span>
    
- <span data-ttu-id="57e21-120">密結合サービスプロバイダーが他の MAPI コンポーネントと対話する場合、密接に結合されていない場合でも、まったく同じように操作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57e21-120">When tightly coupled service providers do interact with other MAPI components, they must still interact with them in exactly the way they would if they were not tightly coupled.</span></span> <span data-ttu-id="57e21-121">たとえば、ユーザーが統合されたメッセージストアプロバイダーとトランスポートプロバイダーを既定のメッセージストアとして使用していて、別のトランスポートプロバイダーを使用してメッセージを送信する場合は、ユーザーが外出中にコンピューターを使用してリモートトランスポート pr に切り替えたときに発生する可能性があります。ovider-密結合サービスプロバイダーのメッセージストア部分は、スタンドアロンのメッセージストアプロバイダーの場合と同様に、MAPI スプーラーと対話する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57e21-121">For example, if a user is using a combined message store provider and transport provider as their default message store but is using a separate transport provider to send messages — as can happen when a user takes a computer on the road and switches to a remote transport provider — the message store portion of the tightly coupled service provider must still interact with MAPI spooler just as if it were a standalone message store provider.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57e21-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="57e21-122">See also</span></span>



[<span data-ttu-id="57e21-123">MAPI メッセージ ストア プロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="57e21-123">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

