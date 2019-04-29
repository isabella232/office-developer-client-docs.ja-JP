---
title: MAPI オブジェクトコンテインメント階層
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 33747835-6eeb-4e07-8f92-3cfa81eecd0f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f5faf3a3d4971b01509d0ff0cfa59451015ba205
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426927"
---
# <a name="mapi-object-containment-hierarchy"></a><span data-ttu-id="b6b6f-103">MAPI オブジェクトコンテインメント階層</span><span class="sxs-lookup"><span data-stu-id="b6b6f-103">MAPI object containment hierarchy</span></span>
  
<span data-ttu-id="b6b6f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6b6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6b6f-105">オブジェクト間のコンテインメント関係は、オブジェクトによっては、他のオブジェクトに対するアクセスの依存関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-105">The containment relationship between objects specifies the dependencies that some objects have on other objects for access.</span></span> <span data-ttu-id="b6b6f-106">クライアントアプリケーションの場合、特定のオブジェクトへのアクセスにより、他のオブジェクトへのアクセスが可能になります。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-106">For a client application, access to particular objects enables access to others.</span></span> <span data-ttu-id="b6b6f-107">場合によっては、サービスプロバイダーによって実装されたオブジェクト間の包含関係が論理階層に従います。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-107">In some cases, the containment relationship between objects implemented by a service provider follows a logical hierarchy.</span></span> <span data-ttu-id="b6b6f-108">その他の場合は任意です。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-108">In other cases, it is arbitrary.</span></span> 
  
<span data-ttu-id="b6b6f-109">クライアントは、他の多くのオブジェクト (サービスプロバイダーや mapi アドレス帳など) を使用する前に、MAPI セッションオブジェクトへのアクセス権を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-109">A client must obtain access to a MAPI session object before it can use many other objects (for example, service providers and the MAPI address book).</span></span>
  
<span data-ttu-id="b6b6f-110">メッセージストアのコンテインメントは、メッセージストア内のオブジェクト (メッセージストアオブジェクト自体、フォルダー、メッセージ、および添付ファイル) 間の階層的な関係に基づいています。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-110">Message store containment is based on the hierarchical relationship between objects in the message store: the message store object itself, folders, messages, and attachments.</span></span> <span data-ttu-id="b6b6f-111">論理的には、添付ファイルはメッセージ、フォルダー内のメッセージ、およびメッセージストア内のフォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-111">Logically, attachments are contained in messages, messages in folders, and folders in the message store.</span></span> <span data-ttu-id="b6b6f-112">コンテインメント関係は、この論理階層に一致します。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-112">The containment relationship matches this logical hierarchy.</span></span> <span data-ttu-id="b6b6f-113">たとえば、メッセージへのアクセスを取得するには、クライアントは最初に、メッセージが含まれているフォルダーにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-113">To gain access to a message, for example, a client must first access the folder in which the message is contained.</span></span> <span data-ttu-id="b6b6f-114">プロファイルおよび状態オブジェクトは、より詳細な包含関係の例です。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-114">Profiles and status objects are examples of a more arbitrary containment relationship.</span></span> <span data-ttu-id="b6b6f-115">これらのオブジェクトはいずれも、セッションを通じて使用できます。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-115">Both of these objects are available through the session.</span></span> 
  
<span data-ttu-id="b6b6f-116">一部のオブジェクトでは、コンテナーが唯一のアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-116">With some objects, containers provide the only access.</span></span> <span data-ttu-id="b6b6f-117">添付ファイルと受信者は、コンテナーに完全に依存するオブジェクトの例です。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-117">Attachments and recipients are examples of objects that are totally dependent on their containers.</span></span> <span data-ttu-id="b6b6f-118">添付ファイルまたは受信者に対する唯一のアクセスは、それが属しているメッセージを使用することです。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-118">The only access to an attachment or a recipient is through the message to which it belongs.</span></span> <span data-ttu-id="b6b6f-119">その他のオブジェクトには、代替アクセスパスがあります。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-119">Other objects have alternate access paths.</span></span> <span data-ttu-id="b6b6f-120">これらのオブジェクトには、エントリ識別子として認識されるバイナリ識別子が、それらを作成するサービスプロバイダーによって割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-120">These objects are assigned binary identifiers, known as entry identifiers, by the service providers that create them.</span></span> <span data-ttu-id="b6b6f-121">エントリ識別子を使用して、オブジェクトに直接アクセスし、クライアントがコンテインメントツリーをバイパスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-121">Entry identifiers can be used to access their objects directly, enabling clients to bypass the containment tree.</span></span> 
  
<span data-ttu-id="b6b6f-122">次の図は、MAPI コンテインメント階層を示しています。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-122">The following illustration shows the MAPI containment hierarchy.</span></span> <span data-ttu-id="b6b6f-123">セッションは、クライアントが他のすべてのオブジェクトにアクセスするセッションを経由するため、ツリーの最上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-123">The session is at the top of the tree because it is through the session that a client gains access to all other objects.</span></span> <span data-ttu-id="b6b6f-124">次のレベルには、メッセージストアテーブル、現在のセッションのすべてのメッセージストアプロバイダーのプロパティを一覧表示した table オブジェクト、およびすべてのアドレス帳プロバイダーへのアクセスを提供するアドレス帳が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-124">The next level includes the message store table, a table object that lists properties for all of the message store providers in the current session, and the address book to supply access to all of the address book providers.</span></span> <span data-ttu-id="b6b6f-125">メッセージストアテーブルとアドレス帳を使用して、次に示すように、特定のサービスプロバイダーによって実装されているオブジェクトに、コンテインメントの順序でアクセスします。</span><span class="sxs-lookup"><span data-stu-id="b6b6f-125">The message store table and address book are used to access the objects implemented by particular service providers, shown next, in containment order.</span></span>
  
<span data-ttu-id="b6b6f-126">**MAPI 含有階層**</span><span class="sxs-lookup"><span data-stu-id="b6b6f-126">**MAPI containment hierarchy**</span></span>
  
<span data-ttu-id="b6b6f-127">![MAPI コンテインメント階層](media/amapi_41.gif "MAPI コンテインメント階層")</span><span class="sxs-lookup"><span data-stu-id="b6b6f-127">![MAPI containment hierarchy](media/amapi_41.gif "MAPI containment hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6b6f-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6b6f-128">See also</span></span>

- [<span data-ttu-id="b6b6f-129">MAPI のオブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="b6b6f-129">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

