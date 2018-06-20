---
title: MAPI オブジェクトの包含階層
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 33747835-6eeb-4e07-8f92-3cfa81eecd0f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 94fea23f71e6bc29b038db38f6f06cda0f85d635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801415"
---
# <a name="mapi-object-containment-hierarchy"></a><span data-ttu-id="40f63-103">MAPI オブジェクトの包含階層</span><span class="sxs-lookup"><span data-stu-id="40f63-103">MAPI object containment hierarchy</span></span>
  
<span data-ttu-id="40f63-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40f63-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40f63-105">オブジェクト間の包含関係は、他のオブジェクトをアクセスするためにいくつかのオブジェクトを持つ依存関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="40f63-105">The containment relationship between objects specifies the dependencies that some objects have on other objects for access.</span></span> <span data-ttu-id="40f63-106">クライアント アプリケーションでは、特定のオブジェクトへのアクセスは他のユーザーへのアクセスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="40f63-106">For a client application, access to particular objects enables access to others.</span></span> <span data-ttu-id="40f63-107">場合によっては、サービス プロバイダーによって実装されたオブジェクトとの間の包含関係に依存して、論理的な階層。</span><span class="sxs-lookup"><span data-stu-id="40f63-107">In some cases, the containment relationship between objects implemented by a service provider follows a logical hierarchy.</span></span> <span data-ttu-id="40f63-108">それ以外の場合は、任意です。</span><span class="sxs-lookup"><span data-stu-id="40f63-108">In other cases, it is arbitrary.</span></span> 
  
<span data-ttu-id="40f63-109">クライアントは、他の多くのオブジェクト (たとえば、サービス プロバイダーと MAPI アドレス帳) を使用する前に MAPI セッション オブジェクトへのアクセスを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40f63-109">A client must obtain access to a MAPI session object before it can use many other objects (for example, service providers and the MAPI address book).</span></span>
  
<span data-ttu-id="40f63-110">メッセージ ストアの抑制は、メッセージ ・ ストア内のオブジェクト間の階層関係に基づいて: メッセージ ・ ストア自体、フォルダー、メッセージ、および添付ファイルのオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="40f63-110">Message store containment is based on the hierarchical relationship between objects in the message store: the message store object itself, folders, messages, and attachments.</span></span> <span data-ttu-id="40f63-111">論理的には、添付ファイルは、メッセージ、フォルダー、およびメッセージ ストア内のフォルダー内のメッセージに含まれます。</span><span class="sxs-lookup"><span data-stu-id="40f63-111">Logically, attachments are contained in messages, messages in folders, and folders in the message store.</span></span> <span data-ttu-id="40f63-112">包含関係では、この論理的な階層と一致します。</span><span class="sxs-lookup"><span data-stu-id="40f63-112">The containment relationship matches this logical hierarchy.</span></span> <span data-ttu-id="40f63-113">メッセージへのアクセスを取得するには、たとえば、クライアント アクセスする必要があります最初メッセージを格納するフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="40f63-113">To gain access to a message, for example, a client must first access the folder in which the message is contained.</span></span> <span data-ttu-id="40f63-114">プロファイルおよび状態オブジェクトは、任意の複数の包含関係の例を示します。</span><span class="sxs-lookup"><span data-stu-id="40f63-114">Profiles and status objects are examples of a more arbitrary containment relationship.</span></span> <span data-ttu-id="40f63-115">これらのオブジェクトは、セッションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="40f63-115">Both of these objects are available through the session.</span></span> 
  
<span data-ttu-id="40f63-116">いくつかのオブジェクトでは、コンテナーは、のみのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="40f63-116">With some objects, containers provide the only access.</span></span> <span data-ttu-id="40f63-117">添付ファイルと受信者は、そのコンテナーに完全に依存しているオブジェクトの例を示します。</span><span class="sxs-lookup"><span data-stu-id="40f63-117">Attachments and recipients are examples of objects that are totally dependent on their containers.</span></span> <span data-ttu-id="40f63-118">添付ファイル、または受信者にのみアクセスでは、メッセージが所属する、です。</span><span class="sxs-lookup"><span data-stu-id="40f63-118">The only access to an attachment or a recipient is through the message to which it belongs.</span></span> <span data-ttu-id="40f63-119">その他のオブジェクトには、代替アクセス パスがあります。</span><span class="sxs-lookup"><span data-stu-id="40f63-119">Other objects have alternate access paths.</span></span> <span data-ttu-id="40f63-120">これらのオブジェクトには、それらを作成するサービス プロバイダーによって、エントリの識別子と呼ばれるバイナリの識別子が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="40f63-120">These objects are assigned binary identifiers, known as entry identifiers, by the service providers that create them.</span></span> <span data-ttu-id="40f63-121">エントリ id は、包含構造ツリーをバイパスするクライアントを有効にすると、オブジェクトに直接アクセスするのには使用できます。</span><span class="sxs-lookup"><span data-stu-id="40f63-121">Entry identifiers can be used to access their objects directly, enabling clients to bypass the containment tree.</span></span> 
  
<span data-ttu-id="40f63-122">MAPI のコンテインメント階層の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="40f63-122">The following illustration shows the MAPI containment hierarchy.</span></span> <span data-ttu-id="40f63-123">セッションはツリーの上部にあるセッションをクライアントが他のすべてのオブジェクトへのアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="40f63-123">The session is at the top of the tree because it is through the session that a client gains access to all other objects.</span></span> <span data-ttu-id="40f63-124">次のレベルには、メッセージ ストアのテーブル、現在のセッションですべてのアドレス帳プロバイダーへのアクセスを提供するアドレス帳のすべてのメッセージ ストア プロバイダーのプロパティを一覧表示するテーブル オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="40f63-124">The next level includes the message store table, a table object that lists properties for all of the message store providers in the current session, and the address book to supply access to all of the address book providers.</span></span> <span data-ttu-id="40f63-125">メッセージ ストアのテーブルとアドレス帳は、包含構造の順序で、次に示す特定のサービス ・ プロバイダーによって実装されたオブジェクトへのアクセスに使用されます。</span><span class="sxs-lookup"><span data-stu-id="40f63-125">The message store table and address book are used to access the objects implemented by particular service providers, shown next, in containment order.</span></span>
  
<span data-ttu-id="40f63-126">**MAPI コンテインメント階層**</span><span class="sxs-lookup"><span data-stu-id="40f63-126">**MAPI containment hierarchy**</span></span>
  
<span data-ttu-id="40f63-127">![MAPI コンテインメント階層](media/amapi_41.gif "MAPI コンテインメント階層")</span><span class="sxs-lookup"><span data-stu-id="40f63-127">![MAPI containment hierarchy](media/amapi_41.gif "MAPI containment hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40f63-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="40f63-128">See also</span></span>

- [<span data-ttu-id="40f63-129">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="40f63-129">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

