---
title: MAPI サービスプロバイダー
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
# <a name="mapi-service-providers"></a><span data-ttu-id="21dfd-103">MAPI サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="21dfd-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="21dfd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21dfd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21dfd-105">サービスプロバイダーには、次の3つの一般的な種類があります。</span><span class="sxs-lookup"><span data-stu-id="21dfd-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="21dfd-106">アドレス帳プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="21dfd-106">Address book providers.</span></span>
    
- <span data-ttu-id="21dfd-107">メッセージストアプロバイダー。</span><span class="sxs-lookup"><span data-stu-id="21dfd-107">Message store providers.</span></span>
    
- <span data-ttu-id="21dfd-108">トランスポートプロバイダー。</span><span class="sxs-lookup"><span data-stu-id="21dfd-108">Transport providers.</span></span>
    
<span data-ttu-id="21dfd-109">アドレス帳とメッセージストアプロバイダーには多くの類似点があります。</span><span class="sxs-lookup"><span data-stu-id="21dfd-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="21dfd-110">これらのユーザーは、オブジェクトのエントリ識別子を作成するために使用する、MAPI で一意の識別子を登録します。</span><span class="sxs-lookup"><span data-stu-id="21dfd-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="21dfd-111">クライアントがアクセスおよび操作できるオブジェクトおよびプロパティの階層を提供します。</span><span class="sxs-lookup"><span data-stu-id="21dfd-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="21dfd-112">container オブジェクトについては、階層テーブルと contents テーブルをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="21dfd-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="21dfd-113">セッション中に発生した変更をクライアントに通知できるように、これらのテーブルに対するイベント通知と、必要に応じて個々のオブジェクトをサポートします。</span><span class="sxs-lookup"><span data-stu-id="21dfd-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="21dfd-114">操作が長くなると、操作の状態をユーザーに通知するための進行状況インジケーターを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="21dfd-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="21dfd-115">クライアントは、 [IAddrBook: imapiprop](iaddrbookimapiprop.md)と[imapiprop: IUnknown](imapisessioniunknown.md)インターフェイスを使用するか、またはサービスプロバイダーインターフェイスのいずれかを直接使用して、アドレス帳とメッセージストアプロバイダーとの間で間接的に通信できます。次の表。</span><span class="sxs-lookup"><span data-stu-id="21dfd-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="21dfd-116">**アドレス帳プロバイダーインターフェイス**</span><span class="sxs-lookup"><span data-stu-id="21dfd-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="21dfd-117">**メッセージストアプロバイダーインターフェイス**</span><span class="sxs-lookup"><span data-stu-id="21dfd-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21dfd-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="21dfd-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="21dfd-119">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="21dfd-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="21dfd-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="21dfd-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="21dfd-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="21dfd-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="21dfd-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="21dfd-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="21dfd-123">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="21dfd-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="21dfd-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="21dfd-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="21dfd-125">トランスポートプロバイダーは、MAPI およびクライアントとの通信と同じ方法で、アドレス帳とメッセージストアプロバイダーとは異なります。</span><span class="sxs-lookup"><span data-stu-id="21dfd-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="21dfd-126">通常、トランスポートプロバイダーは、通信を開始するのではなく、MAPI が情報を求めるメッセージを表示するのを待ちます。</span><span class="sxs-lookup"><span data-stu-id="21dfd-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="21dfd-127">他のプロバイダーとは異なり、トランスポートプロバイダーはクライアントによってよくアクセスされるさまざまなオブジェクトおよびテーブルをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="21dfd-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="21dfd-128">ただし、すべてのサービスプロバイダーと同様に status オブジェクトをサポートし、そのプロパティを状態テーブルに公開します。</span><span class="sxs-lookup"><span data-stu-id="21dfd-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="21dfd-129">アドレス帳およびメッセージストアプロバイダーは、エントリ id を構築するための一意の識別子を登録するために[imapisupport:: setprovideruid](imapisupport-setprovideruid.md)メソッドを呼び出します。トランスポートプロバイダーは、 [IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出します。特定のメッセージを配信する責任を負うために、一意の識別子およびアドレスの種類を登録します。</span><span class="sxs-lookup"><span data-stu-id="21dfd-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="21dfd-130">サービスプロバイダーは3つのヘッダーファイル (1 つのパブリックヘッダーファイルと2つの内部ファイル) を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="21dfd-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="21dfd-131">構成用にパブリックヘッダーファイルを使用し、プロパティとその値を記録します。</span><span class="sxs-lookup"><span data-stu-id="21dfd-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="21dfd-132">必要なすべてのパブリック MAPI ヘッダーを内部ヘッダーファイルのいずれかに含めることができます。このヘッダーファイルは、すべてのサービスプロバイダーのソースファイルに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="21dfd-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="21dfd-133">他の内部ファイルを使用して、リソース識別子を定義します。</span><span class="sxs-lookup"><span data-stu-id="21dfd-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="21dfd-134">アドレス帳、メッセージストア、およびトランスポートプロバイダーは、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="21dfd-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="21dfd-135">エントリポイント関数を指定します。</span><span class="sxs-lookup"><span data-stu-id="21dfd-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="21dfd-136">ログオンと初期化を処理するプロバイダーとログオンオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="21dfd-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="21dfd-137">プロバイダーがメッセージサービスに属している場合は、メッセージサービスエントリポイント関数を指定します。</span><span class="sxs-lookup"><span data-stu-id="21dfd-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="21dfd-138">プロパティシートを実装することで、構成をサポートします。</span><span class="sxs-lookup"><span data-stu-id="21dfd-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="21dfd-139">status オブジェクトを実装し、状態テーブルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="21dfd-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="21dfd-140">シャットダウンを処理します。</span><span class="sxs-lookup"><span data-stu-id="21dfd-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21dfd-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="21dfd-141">See also</span></span>



[<span data-ttu-id="21dfd-142">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="21dfd-142">MAPI Concepts</span></span>](mapi-concepts.md)

