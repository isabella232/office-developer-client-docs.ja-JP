---
title: MAPI サービス プロバイダー
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409539"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="235ab-103">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="235ab-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="235ab-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="235ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="235ab-105">サービス プロバイダーには、次の 3 つの一般的な種類があります。</span><span class="sxs-lookup"><span data-stu-id="235ab-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="235ab-106">アドレス帳プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="235ab-106">Address book providers.</span></span>
    
- <span data-ttu-id="235ab-107">メッセージ ストア プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="235ab-107">Message store providers.</span></span>
    
- <span data-ttu-id="235ab-108">トランスポート プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="235ab-108">Transport providers.</span></span>
    
<span data-ttu-id="235ab-109">アドレス帳とメッセージ ストア プロバイダーには、多くの類似点があります。</span><span class="sxs-lookup"><span data-stu-id="235ab-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="235ab-110">オブジェクトのエントリ識別子を作成するために使用する一意の識別子を MAPI に登録します。</span><span class="sxs-lookup"><span data-stu-id="235ab-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="235ab-111">クライアントがアクセスおよび操作できるオブジェクトとプロパティの階層を提供します。</span><span class="sxs-lookup"><span data-stu-id="235ab-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="235ab-112">コンテナー オブジェクトでは、階層テーブルとコンテンツ テーブルがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="235ab-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="235ab-113">これらのテーブルおよび必要に応じて個々のオブジェクトに対するイベント通知をサポートし、セッション中に発生した変更をクライアントに通知できます。</span><span class="sxs-lookup"><span data-stu-id="235ab-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="235ab-114">操作が長くなると、進行状況インジケーターを表示して、操作の状態をユーザーに通知できます。</span><span class="sxs-lookup"><span data-stu-id="235ab-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="235ab-115">クライアントは [、IAddrBook : IMAPIProp](iaddrbookimapiprop.md) および [IMAPISession : IUnknown](imapisessioniunknown.md) インターフェイスを使用するか、次の表のいずれかのサービス プロバイダー インターフェイスを使用して、MAPI を介して間接的にアドレス帳およびメッセージ ストア プロバイダーと通信できます。</span><span class="sxs-lookup"><span data-stu-id="235ab-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="235ab-116">**アドレス帳プロバイダー インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="235ab-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="235ab-117">**メッセージ ストア プロバイダー インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="235ab-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="235ab-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="235ab-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="235ab-119">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="235ab-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="235ab-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="235ab-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="235ab-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="235ab-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="235ab-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="235ab-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="235ab-123">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="235ab-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="235ab-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="235ab-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="235ab-125">トランスポート プロバイダーは、MAPI とクライアントとの通信方法でアドレス帳プロバイダーやメッセージ ストア プロバイダーとは異なります。</span><span class="sxs-lookup"><span data-stu-id="235ab-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="235ab-126">トランスポート プロバイダーは、通常、MAPI が通信を開始するのではなく、情報の入力を求めるのを待ちます。</span><span class="sxs-lookup"><span data-stu-id="235ab-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="235ab-127">他のプロバイダーとは異なり、トランスポート プロバイダーは、クライアントが一般的にアクセスするさまざまなオブジェクトとテーブルをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="235ab-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="235ab-128">ただし、すべてのサービス プロバイダーと同様に、状態オブジェクトをサポートし、そのプロパティを状態テーブルに発行します。</span><span class="sxs-lookup"><span data-stu-id="235ab-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="235ab-129">アドレス帳とメッセージ ストア プロバイダーは [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) メソッドを呼び出して、エントリ識別子を作成するための一意の識別子を登録します。トランスポート プロバイダーは [、IXPLogon::AddressTypes](ixplogon-addresstypes.md) メソッドを呼び出して一意の識別子を登録し、特定のメッセージの配信の責任を負うアドレスの種類を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="235ab-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="235ab-130">サービス プロバイダーには、1 つのパブリック ヘッダー ファイルと 2 つの内部ファイルという 3 つのヘッダー ファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="235ab-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="235ab-131">構成およびプロパティとその値の文書化には、パブリック ヘッダー ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="235ab-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="235ab-132">内部ヘッダー ファイルの 1 つに、必要なすべてのパブリック MAPI ヘッダーを含めます。このヘッダー ファイルは、すべてのサービス プロバイダー ソース ファイルに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="235ab-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="235ab-133">他の内部ファイルを使用して、リソース識別子を定義します。</span><span class="sxs-lookup"><span data-stu-id="235ab-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="235ab-134">アドレス帳、メッセージ ストア、およびトランスポート プロバイダーは、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="235ab-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="235ab-135">エントリ ポイント関数を指定します。</span><span class="sxs-lookup"><span data-stu-id="235ab-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="235ab-136">ログオンと初期化を処理するプロバイダーとログオン オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="235ab-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="235ab-137">プロバイダーがメッセージ サービスに属している場合は、メッセージ サービスエントリ ポイント関数を指定します。</span><span class="sxs-lookup"><span data-stu-id="235ab-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="235ab-138">プロパティ シートを実装して構成をサポートします。</span><span class="sxs-lookup"><span data-stu-id="235ab-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="235ab-139">status オブジェクトを実装し、状態テーブルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="235ab-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="235ab-140">シャットダウンを処理します。</span><span class="sxs-lookup"><span data-stu-id="235ab-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="235ab-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="235ab-141">See also</span></span>



[<span data-ttu-id="235ab-142">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="235ab-142">MAPI Concepts</span></span>](mapi-concepts.md)

