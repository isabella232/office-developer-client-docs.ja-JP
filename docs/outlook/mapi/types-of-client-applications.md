---
title: クライアントアプリケーションの種類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 167710243c61a7226375b88977c94ff4a517c1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417057"
---
# <a name="types-of-client-applications"></a><span data-ttu-id="fe972-103">クライアントアプリケーションの種類</span><span class="sxs-lookup"><span data-stu-id="fe972-103">Types of Client Applications</span></span>

  
  
<span data-ttu-id="fe972-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe972-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe972-105">主に、個人間メッセージ (IPM) を処理するメッセージングクライアントと、プロセス間通信 (IPC) メッセージを処理するメッセージングクライアントという2種類のメッセージングクライアントがあります。</span><span class="sxs-lookup"><span data-stu-id="fe972-105">There are primarily two types of messaging clients: those that handle interpersonal messages (IPM) and those that handle interprocess communication (IPC) messages.</span></span> <span data-ttu-id="fe972-106">このような種類の場合、メッセージングクライアントアプリケーションは次のように分類できます。</span><span class="sxs-lookup"><span data-stu-id="fe972-106">Within those types, messaging client applications can be categorized as follows:</span></span>
  
- <span data-ttu-id="fe972-107">個人ユーザー</span><span class="sxs-lookup"><span data-stu-id="fe972-107">Person-to-person</span></span>
    
- <span data-ttu-id="fe972-108">ユーザーのコンピューター</span><span class="sxs-lookup"><span data-stu-id="fe972-108">Person-to-machine</span></span>
    
- <span data-ttu-id="fe972-109">コンピューターから個人へ</span><span class="sxs-lookup"><span data-stu-id="fe972-109">Machine-to-person</span></span>
    
- <span data-ttu-id="fe972-110">コンピューター間</span><span class="sxs-lookup"><span data-stu-id="fe972-110">Machine-to-machine</span></span>
    
- <span data-ttu-id="fe972-111">人とコンピューターの組み合わせ</span><span class="sxs-lookup"><span data-stu-id="fe972-111">Mix of persons and machines</span></span>
    
<span data-ttu-id="fe972-112">個人間のアプリケーションでは、メッセージの交換を開始し、別のユーザーに応答します。</span><span class="sxs-lookup"><span data-stu-id="fe972-112">Person-to-person applications involve a person initiating the exchange of messages and another person responding.</span></span> <span data-ttu-id="fe972-113">このカテゴリのアプリケーションには、従来の電子メールアプリケーションだけでなく、ドキュメントのルーティングや経費の承認など、より構造化された交換が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fe972-113">This category of applications includes traditional email applications as well as more structured exchanges such as document routing or expense approval.</span></span>
  
<span data-ttu-id="fe972-114">個人間のアプリケーションでは、メッセージの交換を開始するユーザーとコンピューターが応答します。</span><span class="sxs-lookup"><span data-stu-id="fe972-114">Person-to-machine applications involve a person initiating the exchange of messages and a machine responding.</span></span> <span data-ttu-id="fe972-115">このカテゴリには、電子メールを使用して、データベースクエリを送信したり、メーリングリストにサブスクライブしたりするアプリケーションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fe972-115">This category includes applications that use email to, for example, submit a database query or subscribe to a mailing list.</span></span>
  
<span data-ttu-id="fe972-116">コンピュータツーユーザーアプリケーションには、メッセージの交換を開始するコンピューターと、ユーザーが応答することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fe972-116">Machine-to-person applications involve a machine initiating the exchange of messages and a person responding.</span></span> <span data-ttu-id="fe972-117">このカテゴリには、ニュースフィードや意見の調査などのドキュメントを配布するアプリケーションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fe972-117">This category includes applications that distribute documents such as news feeds and opinion surveys.</span></span>
  
<span data-ttu-id="fe972-118">コンピューター間アプリケーションには、メッセージの交換を開始するコンピューターと、コンピューターが応答することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fe972-118">Machine-to-machine applications involve a machine initiating the exchange of messages and a machine responding.</span></span> <span data-ttu-id="fe972-119">このカテゴリには、リンクのハートビートの監視、ディレクトリおよびデータベースレプリケーションなどのアプリケーションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fe972-119">This category includes applications such as link heartbeat monitoring and directory and database replication.</span></span>
  
<span data-ttu-id="fe972-120">最終的なカテゴリである人と機械が混在している場合は、より複雑なシナリオが必要になります。</span><span class="sxs-lookup"><span data-stu-id="fe972-120">The final category, a mix of persons and machines, involves a more complex scenario.</span></span> <span data-ttu-id="fe972-121">このカテゴリには、送信者と受信者との間でメッセージを必ずしも転送しないアプリケーションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fe972-121">This category includes applications that do not necessarily transmit messages between senders and recipients.</span></span> <span data-ttu-id="fe972-122">代わりに、パブリックフォルダーまたはメッセージストアでサポートされている web サイトフォーラムに直接投稿することができます。</span><span class="sxs-lookup"><span data-stu-id="fe972-122">Instead they might post them directly into a public folder or to a web-site forum supported by a message store.</span></span> <span data-ttu-id="fe972-123">その後、他の閲覧者、管理者、またはソフトウェアエージェントがメッセージを必要に応じて消費することができます。</span><span class="sxs-lookup"><span data-stu-id="fe972-123">The messages can then be consumed on demand by other readers, an administrator, or a software agent.</span></span>
  
<span data-ttu-id="fe972-124">個人間アプリケーション、コンピューターから個人アプリケーション、またはパブリックフォーラムにメッセージを投稿するアプリケーションを作成している場合は、IPM メッセージを送受信するようにアプリケーションを設計します。</span><span class="sxs-lookup"><span data-stu-id="fe972-124">If you are writing a person-to-person application, machine-to-person application, or an application that posts messages to public forums, design your application to send and receive IPM messages.</span></span> <span data-ttu-id="fe972-125">ユーザーとコンピューターの間のアプリケーションを記述する場合は、IPC メッセージを送受信するように設計できます。</span><span class="sxs-lookup"><span data-stu-id="fe972-125">If you are writing a person-to-machine or machine-to-machine application, it can be designed to send and receive IPC messages.</span></span> <span data-ttu-id="fe972-126">人間のユーザーの操作を必要とするアプリケーションは、IPM メッセージをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe972-126">Any application that requires the interaction of a human user must support IPM messages.</span></span> <span data-ttu-id="fe972-127">さまざまなシナリオで、ユーザーとコンピューターの両方に関係するアプリケーションは、多くの場合、IPM および IPC メッセージの両方をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe972-127">Applications that involve both people and machines in a variety of scenarios often must support both IPM and IPC messages.</span></span> <span data-ttu-id="fe972-128">2つのクラスの唯一の相違点は、メッセージストア内の IPM メッセージがメッセージングクライアントのユーザーに表示されるのに対して、IPC メッセージは通常、クライアントアプリケーションユーザーには表示されないことです。</span><span class="sxs-lookup"><span data-stu-id="fe972-128">The only real difference between the two classes is that IPM messages in a message store are visible to users of messaging clients, while IPC messages usually are not visible to the client application users.</span></span> 
  
<span data-ttu-id="fe972-129">MAPI スーパークラス、IPM および ipc によって提供される機能にメッセージを制限するのではなく、新しい IPM または ipc サブクラスを作成することで、これらのクラスをカスタマイズし、強化することができます。</span><span class="sxs-lookup"><span data-stu-id="fe972-129">Rather than limiting your messages to the capabilities provided by the MAPI superclasses, IPM and IPC, you can customize and enhance these classes by creating new IPM or IPC subclasses.</span></span> <span data-ttu-id="fe972-130">メッセージサブクラスを作成するには、スーパークラスから継承する inventing の新しいメッセージクラスが必要です。</span><span class="sxs-lookup"><span data-stu-id="fe972-130">Creating message subclasses involves inventing new message classes that inherit from the superclasses.</span></span> <span data-ttu-id="fe972-131">たとえば、個人間のアプリケーションが顧客関係管理に特化している場合は、ipm を定義することによって、ipm スーパークラスをサブクラス化することができます。Contact. customer クラスと顧客を説明するプロパティを作成します。</span><span class="sxs-lookup"><span data-stu-id="fe972-131">For example, if your person-to-person application specializes in customer relationship management, you can subclass the IPM superclass by defining an IPM.Contact.Customer class and create properties that describe a customer.</span></span> <span data-ttu-id="fe972-132">これらのカスタムプロパティをサポートするだけでなく、IPM.Contact。顧客メッセージは、すべての IPM メッセージでサポートされているプロパティを継承します。</span><span class="sxs-lookup"><span data-stu-id="fe972-132">In addition to supporting these custom properties, your IPM.Contact.Customer messages will inherit the properties supported by all IPM messages.</span></span>
  

