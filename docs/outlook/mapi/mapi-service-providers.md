---
title: MAPI サービス プロバイダー
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3f1cab24ef6bbd632ee3dc204e93f59e6f9ac846
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801466"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="96896-103">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="96896-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="96896-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96896-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96896-105">次の 3 つの一般的なサービス ・ プロバイダーの種類があります。</span><span class="sxs-lookup"><span data-stu-id="96896-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="96896-106">アドレス帳プロバイダーをします。</span><span class="sxs-lookup"><span data-stu-id="96896-106">Address book providers.</span></span>
    
- <span data-ttu-id="96896-107">メッセージ ストア プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="96896-107">Message store providers.</span></span>
    
- <span data-ttu-id="96896-108">プロバイダーに転送します。</span><span class="sxs-lookup"><span data-stu-id="96896-108">Transport providers.</span></span>
    
<span data-ttu-id="96896-109">アドレス帳、メッセージ ストア プロバイダーでは、多くの類似点があります。</span><span class="sxs-lookup"><span data-stu-id="96896-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="96896-110">MAPI を使用して、オブジェクトのエントリ id を作成するために一意の識別子を登録するとします。</span><span class="sxs-lookup"><span data-stu-id="96896-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="96896-111">オブジェクトとクライアントがアクセスしたり、操作したりするプロパティの階層を提供します。</span><span class="sxs-lookup"><span data-stu-id="96896-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="96896-112">コンテナーのオブジェクトには、階層テーブルおよび内容のテーブルをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="96896-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="96896-113">サポート イベント通知これらのテーブルにし、必要に応じて個々 のオブジェクトのクライアントは、セッション中に発生する変更通知できるようにします。</span><span class="sxs-lookup"><span data-stu-id="96896-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="96896-114">操作には時間がかかるになると、操作のステータスをユーザーに通知する進行状況インジケーターを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="96896-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="96896-115">クライアントと通信できますアドレス帳、メッセージ ストア プロバイダーから間接的に、MAPI を使用して、 [IAddrBook: IMAPIProp](iaddrbookimapiprop.md)と[IMAPISession: IUnknown](imapisessioniunknown.md)インタ フェースまたは直接のサービス プロバイダー インターフェイスのいずれかを使用して、次の表。</span><span class="sxs-lookup"><span data-stu-id="96896-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="96896-116">**アドレス帳プロバイダー インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="96896-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="96896-117">**メッセージ ストア プロバイダーのインターフェイス**</span><span class="sxs-lookup"><span data-stu-id="96896-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96896-118">これにより: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="96896-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="96896-119">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="96896-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="96896-120">IDistList: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="96896-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="96896-121">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="96896-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="96896-122">IMailUser: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="96896-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="96896-123">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="96896-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="96896-124">IAttach: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="96896-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="96896-125">トランスポート プロバイダーは、クライアントで MAPI と通信する方法で、アドレス帳、メッセージ ストア プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="96896-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="96896-126">トランスポート プロバイダーは、通常の通信を開始するのではなく、情報を要求するには MAPI の待機します。</span><span class="sxs-lookup"><span data-stu-id="96896-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="96896-127">他のプロバイダーとは異なりトランスポート プロバイダーはさまざまなオブジェクトとクライアントが頻繁にアクセスされるテーブルをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="96896-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="96896-128">ただし、サポートして状態オブジェクトでは、すべてのサービス プロバイダーの操作を行い、状態テーブル内のプロパティを公開します。</span><span class="sxs-lookup"><span data-stu-id="96896-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="96896-129">トランスポート プロバイダーがする[IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出しますが、アドレス帳、メッセージ ストア プロバイダーは、それらのエントリの識別子を構築するための一意の識別子を登録するのには[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出して、処理の特定のメッセージの配信のための一意の識別子とアドレスの種類を登録します。</span><span class="sxs-lookup"><span data-stu-id="96896-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="96896-130">サービス ・ プロバイダーは次の 3 つのヘッダー ファイルで必要があります: 1 つのパブリック ヘッダー ファイルと 2 つの内部のファイルです。</span><span class="sxs-lookup"><span data-stu-id="96896-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="96896-131">パブリック ヘッダー ファイルは、構成し、プロパティとその値を記録するために使用します。</span><span class="sxs-lookup"><span data-stu-id="96896-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="96896-132">内部ヘッダー ファイルのいずれかですべての必要なパブリック MAPI ヘッダーが含まれますこのヘッダー ファイルは、すべてのサービス プロバイダーのソース ファイルに入れるべき。</span><span class="sxs-lookup"><span data-stu-id="96896-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="96896-133">その他の内部のファイルを使用すると、リソース識別子を定義します。</span><span class="sxs-lookup"><span data-stu-id="96896-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="96896-134">アドレス帳、メッセージ ・ ストア、およびトランスポート プロバイダーは、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="96896-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="96896-135">エントリ ポイント関数を指定します。</span><span class="sxs-lookup"><span data-stu-id="96896-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="96896-136">ログオンや初期化を処理するには、プロバイダーとログオン オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="96896-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="96896-137">メッセージ サービス プロバイダーが属している場合は、メッセージ サービスのエントリ ポイント関数を指定します。</span><span class="sxs-lookup"><span data-stu-id="96896-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="96896-138">プロパティ シートを実装することによって構成をサポートします。</span><span class="sxs-lookup"><span data-stu-id="96896-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="96896-139">状態オブジェクトを実装し、状態テーブルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="96896-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="96896-140">ハンドルはシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="96896-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96896-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="96896-141">See also</span></span>



[<span data-ttu-id="96896-142">MAPI �̊T�O</span><span class="sxs-lookup"><span data-stu-id="96896-142">MAPI Concepts</span></span>](mapi-concepts.md)

