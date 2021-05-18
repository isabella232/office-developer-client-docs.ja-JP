---
title: 緊密に結合されたメッセージ ストア プロバイダー
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
# <a name="tightly-coupled-message-store-providers"></a><span data-ttu-id="33011-103">緊密に結合されたメッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="33011-103">Tightly Coupled Message Store Providers</span></span>

  
  
<span data-ttu-id="33011-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33011-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33011-105">メッセージ ストア プロバイダーは、トランスポート プロバイダーと緊密に結合できます。</span><span class="sxs-lookup"><span data-stu-id="33011-105">Message store providers can be tightly coupled with a transport provider.</span></span> <span data-ttu-id="33011-106">MAPI サービス プロバイダーの緊密な結合とは、ストア プロバイダーとトランスポート プロバイダーが通信してメッセージの送受信プロセスをより効率的に行う 2 つのプロバイダーを実装する方法を意味します。</span><span class="sxs-lookup"><span data-stu-id="33011-106">Tightly coupling MAPI service providers means implementing the two providers such that the store provider and transport provider can communicate to make the process of sending and receiving messages more efficient.</span></span> <span data-ttu-id="33011-107">これを行う利点は、MAPI スプーラーではなく、2 つのサービス プロバイダーが相互に直接やり取りできる場合に、パフォーマンスが向上する可能性がある点です。</span><span class="sxs-lookup"><span data-stu-id="33011-107">The benefit of doing this is that performance improvements can result when two service providers can interact with each other directly rather than by means of MAPI spooler.</span></span> <span data-ttu-id="33011-108">メッセージ ストア プロバイダーをトランスポート プロバイダーに緊密に結合するには、トランスポート プロバイダーは、メッセージ ストア プロバイダーのエントリ識別子を MAPI 状態テーブルのトランスポート プロバイダーの行の **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) プロパティに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33011-108">To tightly couple a message store provider to a transport provider, the transport provider must place the message store provider's entry identifier in the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in the transport provider's row in the MAPI status table.</span></span> <span data-ttu-id="33011-109">これにより、MAPI スプーラーはストア プロバイダーをトランスポート プロバイダーに接続できます。</span><span class="sxs-lookup"><span data-stu-id="33011-109">This enables MAPI spooler to connect the store provider to the transport provider.</span></span>
  
<span data-ttu-id="33011-110">メッセージ ストア プロバイダーを他のサービス プロバイダーと緊密に結合する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="33011-110">There is no requirement that a message store provider ever be tightly coupled with any other service provider.</span></span> <span data-ttu-id="33011-111">メッセージ ストア プロバイダーと緊密に結合する最も一般的なサービス プロバイダーは、トランスポート プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="33011-111">The most common service provider to tightly couple with a message store provider is a transport provider.</span></span> <span data-ttu-id="33011-112">これは通常、MAPI スプーラーを使用せずにメッセージの送受信を行う目的で行われます。</span><span class="sxs-lookup"><span data-stu-id="33011-112">This is usually done so that sending and receiving messages can be accomplished without involving the MAPI spooler.</span></span> <span data-ttu-id="33011-113">たとえば、ユーザーが送信メッセージを送信すると、結合されたメッセージ ストア プロバイダーとトランスポート プロバイダーが直接送信できます。</span><span class="sxs-lookup"><span data-stu-id="33011-113">For example, when the user submits an outgoing message, the combined message store provider and transport provider can send it directly.</span></span> <span data-ttu-id="33011-114">結合されたサービス プロバイダーは、まず、処理する新しいメッセージが存在する MAPI スプーラーに通知し、MAPI スプーラーがメッセージ ストア プロバイダーからトランスポート プロバイダーにメッセージを転送するプロセスを開始するのを待つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="33011-114">The combined service providers do not have to first notify MAPI spooler that there is a new message to process and then wait for MAPI spooler to initiate the process of transferring the message from the message store provider to the transport provider.</span></span> <span data-ttu-id="33011-115">これは、ユーザーのコンピューターとサーバー間のネットワーク トラフィックを最小限に抑えることによって、サーバー ベースのメッセージ ストアを使用する場合に特に利点があります。</span><span class="sxs-lookup"><span data-stu-id="33011-115">This has particular benefits when a server-based message store is being used by minimizing network traffic between the user's computer and the server.</span></span>
  
<span data-ttu-id="33011-116">一般に、サービス プロバイダーを緊密に結合する手順は指定されていません。</span><span class="sxs-lookup"><span data-stu-id="33011-116">In general, there are no well-specified procedures for tightly coupling service providers.</span></span> <span data-ttu-id="33011-117">ただし、次のガイドラインを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33011-117">However, you should use the following guidelines:</span></span>
  
- <span data-ttu-id="33011-118">サービス プロバイダーを緊密に結合する理由がパフォーマンスである場合は、結合が MAPI サブシステムの一部を、それらのパーツが通常関与するプロセスから取り出すことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="33011-118">If the reason for tightly coupling service providers is performance, be aware that the coupling takes parts of the MAPI subsystem out of the processes that those parts would normally be involved in.</span></span> <span data-ttu-id="33011-119">これは、結合されたサービス プロバイダー内の個々のパーツが、通常は使用されていない MAPI サブシステムの部分との相互作用をシミュレートする方法で相互に対話する必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="33011-119">This implies that the individual parts in the combined service provider should interact with each other in a way that simulates the interaction they would normally have with the parts of the MAPI subsystem that are not being used.</span></span>
    
- <span data-ttu-id="33011-120">緊密に結合されたサービス プロバイダーが他の MAPI コンポーネントとやり取りする場合でも、密に結合されていない場合とまったく同じ方法で操作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33011-120">When tightly coupled service providers do interact with other MAPI components, they must still interact with them in exactly the way they would if they were not tightly coupled.</span></span> <span data-ttu-id="33011-121">たとえば、ユーザーが既定のメッセージ ストアとして結合されたメッセージ ストア プロバイダーとトランスポート プロバイダーを使用しているが、別のトランスポート プロバイダーを使用してメッセージを送信している場合は、ユーザーが道路上のコンピューターを使用してリモート トランスポート プロバイダーに切り替える場合に発生します。密結合されたサービス プロバイダーのメッセージ ストア部分は、スタンドアロン メッセージ ストア プロバイダーである場合と同様に、MAPI スプーラーとやり取りする必要があります。</span><span class="sxs-lookup"><span data-stu-id="33011-121">For example, if a user is using a combined message store provider and transport provider as their default message store but is using a separate transport provider to send messages — as can happen when a user takes a computer on the road and switches to a remote transport provider — the message store portion of the tightly coupled service provider must still interact with MAPI spooler just as if it were a standalone message store provider.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33011-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="33011-122">See also</span></span>



[<span data-ttu-id="33011-123">MAPI メッセージ ストア プロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="33011-123">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

