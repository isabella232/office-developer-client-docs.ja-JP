---
title: 密結合のメッセージ ストア プロバイダー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 83ebb739302ca0e12604b9eaf854f273554826ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804101"
---
# <a name="tightly-coupled-message-store-providers"></a><span data-ttu-id="40204-103">密結合のメッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="40204-103">Tightly Coupled Message Store Providers</span></span>

  
  
<span data-ttu-id="40204-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40204-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40204-105">メッセージ ストア プロバイダーは、トランスポート プロバイダーと密接に関連することができます。</span><span class="sxs-lookup"><span data-stu-id="40204-105">Message store providers can be tightly coupled with a transport provider.</span></span> <span data-ttu-id="40204-106">ストア プロバイダーが、トランスポート プロバイダーは、プロセスをより効率的にメッセージを送受信するために通信できるように、2 つのプロバイダーを実装する MAPI サービス プロバイダーの手段が緊密に結び付けられます。</span><span class="sxs-lookup"><span data-stu-id="40204-106">Tightly coupling MAPI service providers means implementing the two providers such that the store provider and transport provider can communicate to make the process of sending and receiving messages more efficient.</span></span> <span data-ttu-id="40204-107">この方法の利点は、MAPI スプーラーを使用してではなく、相互に直接対話できる 2 つのサービス プロバイダーとパフォーマンスの向上が発生することです。</span><span class="sxs-lookup"><span data-stu-id="40204-107">The benefit of doing this is that performance improvements can result when two service providers can interact with each other directly rather than by means of MAPI spooler.</span></span> <span data-ttu-id="40204-108">トランスポート プロバイダーにメッセージ ストア プロバイダーが密に結合するには、トランスポート プロバイダーでは、トランスポート プロバイダーの**PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) のプロパティで、メッセージ ストア プロバイダーのエントリの識別子を置く必要があります。MAPI 状態テーブル内の行です。</span><span class="sxs-lookup"><span data-stu-id="40204-108">To tightly couple a message store provider to a transport provider, the transport provider must place the message store provider's entry identifier in the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in the transport provider's row in the MAPI status table.</span></span> <span data-ttu-id="40204-109">これにより、MAPI スプーラーを無効にして、トランスポート プロバイダーは、ストア プロバイダーに接続できます。</span><span class="sxs-lookup"><span data-stu-id="40204-109">This enables MAPI spooler to connect the store provider to the transport provider.</span></span>
  
<span data-ttu-id="40204-110">メッセージ ストア プロバイダーが密に結合する他のサービス プロバイダーの要件はありません。</span><span class="sxs-lookup"><span data-stu-id="40204-110">There is no requirement that a message store provider ever be tightly coupled with any other service provider.</span></span> <span data-ttu-id="40204-111">メッセージ ストア プロバイダーと密に結合する最も一般的なサービス ・ プロバイダーは、トランスポート プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="40204-111">The most common service provider to tightly couple with a message store provider is a transport provider.</span></span> <span data-ttu-id="40204-112">これは、通常送信するようにし、メッセージの受信は、MAPI スプーラーを使用することがなく行うことができます。</span><span class="sxs-lookup"><span data-stu-id="40204-112">This is usually done so that sending and receiving messages can be accomplished without involving the MAPI spooler.</span></span> <span data-ttu-id="40204-113">たとえば、ユーザーは、送信メッセージを送信するときに結合されたメッセージ ストア プロバイダーおよびトランスポート プロバイダー送信ことができます直接。</span><span class="sxs-lookup"><span data-stu-id="40204-113">For example, when the user submits an outgoing message, the combined message store provider and transport provider can send it directly.</span></span> <span data-ttu-id="40204-114">結合されたサービス プロバイダーは、まず MAPI スプーラーに通知を処理し、MAPI スプーラーを無効するトランスポート プロバイダーは、メッセージ ストア プロバイダーからのメッセージを転送するプロセスを開始するまで待機し、新しいメッセージが表示されることはありません。</span><span class="sxs-lookup"><span data-stu-id="40204-114">The combined service providers do not have to first notify MAPI spooler that there is a new message to process and then wait for MAPI spooler to initiate the process of transferring the message from the message store provider to the transport provider.</span></span> <span data-ttu-id="40204-115">サーバー ベースのメッセージ ストアは、ユーザーのコンピューターとサーバー間のネットワーク トラフィックを最小限に抑えることで使用されているときに特別なメリットがあります。</span><span class="sxs-lookup"><span data-stu-id="40204-115">This has particular benefits when a server-based message store is being used by minimizing network traffic between the user's computer and the server.</span></span>
  
<span data-ttu-id="40204-116">一般に、サービス プロバイダーに緊密に結合する明確に定義されたプロシージャではありません。</span><span class="sxs-lookup"><span data-stu-id="40204-116">In general, there are no well-specified procedures for tightly coupling service providers.</span></span> <span data-ttu-id="40204-117">ただし、次のガイドラインを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40204-117">However, you should use the following guidelines:</span></span>
  
- <span data-ttu-id="40204-118">サービス プロバイダーに緊密に結合するためにパフォーマンスがある場合は、結合度がこれらの部分とに関与している通常のプロセスからの MAPI サブシステムの一部を受け取ることに注意します。</span><span class="sxs-lookup"><span data-stu-id="40204-118">If the reason for tightly coupling service providers is performance, be aware that the coupling takes parts of the MAPI subsystem out of the processes that those parts would normally be involved in.</span></span> <span data-ttu-id="40204-119">これは、MAPI サブシステムの使用されていない部分があるが通常の相互作用をシミュレートする方法で、結合されたサービス プロバイダーでは、個々 の部品が相互にやり取りする必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="40204-119">This implies that the individual parts in the combined service provider should interact with each other in a way that simulates the interaction they would normally have with the parts of the MAPI subsystem that are not being used.</span></span>
    
- <span data-ttu-id="40204-120">密結合のサービス ・ プロバイダーは対話するとき、他の MAPI コンポーネントと、必要がありますまだ操作密に結合されていない場合と同じようにします。</span><span class="sxs-lookup"><span data-stu-id="40204-120">When tightly coupled service providers do interact with other MAPI components, they must still interact with them in exactly the way they would if they were not tightly coupled.</span></span> <span data-ttu-id="40204-121">ユーザーは、結合されたメッセージ ストア プロバイダーおよびトランスポート プロバイダーを使用して、既定のメッセージ ストアとしては、別のトランスポート プロバイダーを使用してメッセージを送信する場合など、ユーザーが外出先でコンピューターを実行し、リモート トランスポート pr に切り替えるときに発生することができます、ovider、緊密に結合されたサービス プロバイダーのメッセージ ストアの一部も協力し、MAPI スプーラー スタンドアロン メッセージ ストア プロバイダーの場合と同様です。</span><span class="sxs-lookup"><span data-stu-id="40204-121">For example, if a user is using a combined message store provider and transport provider as their default message store but is using a separate transport provider to send messages — as can happen when a user takes a computer on the road and switches to a remote transport provider — the message store portion of the tightly coupled service provider must still interact with MAPI spooler just as if it were a standalone message store provider.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40204-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="40204-122">See also</span></span>



<span data-ttu-id="40204-123">[MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="40204-123">[Developing a MAPI Message Store Provider](developing-a-mapi-message-store-provider.md)</span></span>

