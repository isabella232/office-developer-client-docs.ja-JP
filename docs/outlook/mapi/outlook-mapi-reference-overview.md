---
title: Outlook MAPI リファレンス概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: '最終更新日: 2013 年 2 月 1 日'
localization_priority: Priority
ms.openlocfilehash: dc743824cf96800c32d4b4006ae86fbff0bd48a0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723020"
---
# <a name="outlook-mapi-reference-overview"></a><span data-ttu-id="64b58-103">Outlook MAPI リファレンス概要</span><span class="sxs-lookup"><span data-stu-id="64b58-103">Outlook MAPI Reference Overview</span></span>

<span data-ttu-id="64b58-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64b58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64b58-105">このトピックでは、Outlook 2013 MAPI リファレンス ドキュメントに関する概要情報を示します。</span><span class="sxs-lookup"><span data-stu-id="64b58-105">This topic provides overview information about the Outlook 2013 MAPI Reference documentation.</span></span>
  
## <a name="about-this-documentation"></a><span data-ttu-id="64b58-106">このドキュメントについて</span><span class="sxs-lookup"><span data-stu-id="64b58-106">About this documentation</span></span>

<span data-ttu-id="64b58-107">このドキュメントは、Microsoft Outlook 2013 のメッセージ API (MAPI) の実装に適用されます。</span><span class="sxs-lookup"><span data-stu-id="64b58-107">This documentation applies to the implementation of the Messaging API (MAPI) in Microsoft Outlook 2013.</span></span> 
  
<span data-ttu-id="64b58-108">Microsoft Office Outlook 2007 より前の MAPI プログラマーズ リファレンスは、Microsoft Exchange ドキュメントの一部でした。</span><span class="sxs-lookup"><span data-stu-id="64b58-108">Previous to Microsoft Office Outlook 2007, the MAPI Programmer's Reference was part of the Microsoft Exchange documentation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="64b58-109">Microsoft Exchange Server 2007 以降の Exchange では MAPI の使用が重視されていないため、Exchange 実装のサポートは制限されています。</span><span class="sxs-lookup"><span data-stu-id="64b58-109">Because Exchange has deemphasized the use of MAPI since Microsoft Exchange Server 2007, support for the Exchange implementation is limited.</span></span> 
  
<span data-ttu-id="64b58-110">MAPI の Outlook 実装は、Microsoft Exchange の実装とは異なります。</span><span class="sxs-lookup"><span data-stu-id="64b58-110">The Outlook implementation of MAPI differs from the Microsoft Exchange implementation.</span></span> <span data-ttu-id="64b58-111">Outlook の実装は、クライアント コンピューターでの実行に最適化されていて、待機時間の短さが重視されています。</span><span class="sxs-lookup"><span data-stu-id="64b58-111">The Outlook implementation is optimized for running on client computers and emphasizes low latency.</span></span> <span data-ttu-id="64b58-112">Exchange の実装は、高可用性とマルチスレッド処理の優秀さが重要になるサーバーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="64b58-112">The Exchange implementation is intended for servers where high availability and better multithreading are important.</span></span>
  
<span data-ttu-id="64b58-113">このドキュメントは、エンド ユーザーのシステムで実行するアプリケーションに使用してください。</span><span class="sxs-lookup"><span data-stu-id="64b58-113">Use this documentation for applications running on end-user systems.</span></span> <span data-ttu-id="64b58-114">サーバー アプリケーションについては、MAPI の Exchange 実装を使用してください (適切な場合)。または、現行の Exchange API (Exchange Web サービスなど) を使用してください。</span><span class="sxs-lookup"><span data-stu-id="64b58-114">For server applications, use the Exchange implementation of MAPI if appropriate, or use current Exchange APIs such as Exchange Web Services.</span></span> <span data-ttu-id="64b58-115">Exchange Web サービスの詳細については、「[Exchange Web サービスのリファレンス](https://msdn.microsoft.com/library/bb204119.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64b58-115">For more information on Exchange Web Services, see the [Exchange Web Services Reference](https://msdn.microsoft.com/library/bb204119.aspx).</span></span>
  
<span data-ttu-id="64b58-116">MAPI の Outlook 実装または Exchange 実装のどちらでも動作するアプリケーションを作成することは可能です。</span><span class="sxs-lookup"><span data-stu-id="64b58-116">It may be possible to write applications that work with either the Outlook or Exchange implementations of MAPI.</span></span> <span data-ttu-id="64b58-117">たとえば、MFCMAPI はどちらのプラットフォームでも適切に動作します。</span><span class="sxs-lookup"><span data-stu-id="64b58-117">For example, MFCMAPI works well on either platform.</span></span> <span data-ttu-id="64b58-118">実装には多数の共通機能がありますが、明確な相違点と微妙な相違点の両方が存在します。</span><span class="sxs-lookup"><span data-stu-id="64b58-118">The implementations have many common features, but there are differences both obvious and subtle.</span></span> <span data-ttu-id="64b58-119">すべての環境でアプリケーションが動作するようにするには、両方のプラットフォームで十分にテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="64b58-119">You will have to test carefully on both platforms if you intend for your application to work in all environments.</span></span> <span data-ttu-id="64b58-120">このテストには 2 つのシステムが必要になります。これは、同じオペレーティング システムのインストール環境で両方の実装を実行することはサポートされていないためです。</span><span class="sxs-lookup"><span data-stu-id="64b58-120">This testing will require two systems because running both implementations on the same operating system installation is not supported.</span></span>
  
<span data-ttu-id="64b58-121">MAPI は、MAPI ストア内のデータへのローレベル アクセスや、トランスポート、メッセージストア、アドレス帳プロバイダーの作成に適しています。</span><span class="sxs-lookup"><span data-stu-id="64b58-121">Be aware that MAPI is appropriate for low-level access to data in a MAPI store or for building a transport, message store, or address book provider.</span></span> <span data-ttu-id="64b58-122">MAPI は Outlook のビジネス ロジックをバイパスするため、ソリューションの作成の際に API を評価するときには、Outlook オブジェクト モデルの使用についても検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64b58-122">Because MAPI bypasses Outlook's business logic, you should also consider the use of the Outlook object model when you evaluate APIs for building your solution.</span></span> <span data-ttu-id="64b58-123">Outlook オブジェクト モデルは Outlook ビジネス ロジックをカプセル化しますが、マルチスレッド コード、同期プロバイダー、または Windows サービス アプリケーションには適していません。</span><span class="sxs-lookup"><span data-stu-id="64b58-123">The Outlook object model does encapsulate Outlook business logic but is not suitable for multithreaded code, sync providers, or Windows Service applications.</span></span>
  
<span data-ttu-id="64b58-124">このエディションの新機能の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="64b58-124">For information about what is new in this edition, see the following topics:</span></span>
  
- [<span data-ttu-id="64b58-125">このエディションの新機能</span><span class="sxs-lookup"><span data-stu-id="64b58-125">What's New in This Edition</span></span>](what-s-new-in-this-edition.md)
    
- [<span data-ttu-id="64b58-126">このエディションで非推奨の API 要素</span><span class="sxs-lookup"><span data-stu-id="64b58-126">API Elements Deprecated in This Edition</span></span>](api-elements-deprecated-in-this-edition.md)
    
<span data-ttu-id="64b58-127">Outlook 用の MAPI アプリケーションを初めて開発する場合は、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="64b58-127">If you are new to developing MAPI applications for Outlook, see the following topics:</span></span>
  
- [<span data-ttu-id="64b58-128">Outlook 2013 用のソリューションを開発するための API またはテクノロジの選択</span><span class="sxs-lookup"><span data-stu-id="64b58-128">Selecting an API or technology for developing solutions for Outlook 2013</span></span>](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [<span data-ttu-id="64b58-129">よく使用されるヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="64b58-129">Commonly Used Header Files</span></span>](commonly-used-header-files.md)
    
- [<span data-ttu-id="64b58-130">よく使用されるプロパティ</span><span class="sxs-lookup"><span data-stu-id="64b58-130">Commonly Used Properties</span></span>](commonly-used-properties.md)
    
- [<span data-ttu-id="64b58-131">よく使用されるオブジェクト</span><span class="sxs-lookup"><span data-stu-id="64b58-131">Commonly Used Objects</span></span>](commonly-used-objects.md)
    
<span data-ttu-id="64b58-132">このリファレンスの残りの部分は、次の 3 種類の情報に分類されています。</span><span class="sxs-lookup"><span data-stu-id="64b58-132">The rest of this reference is categorized into the following three types of information:</span></span>
  
- <span data-ttu-id="64b58-133">[MAPI のサンプル](mapi-samples.md): さまざまな API 要素の使用法と、基本的な MAPI プロバイダーの実装方法および Outlook アイテムの作成方法を示す多数のコード サンプルに誘導します。</span><span class="sxs-lookup"><span data-stu-id="64b58-133">[MAPI Samples](mapi-samples.md) - Directs you to many code samples that show the use of various API elements and how to implement basic MAPI providers and create Outlook items.</span></span> 
    
- <span data-ttu-id="64b58-134">[MAPI の概念](mapi-concepts.md): MAPI の概念とアーキテクチャについて説明します。</span><span class="sxs-lookup"><span data-stu-id="64b58-134">[MAPI Concepts](mapi-concepts.md) - Explains the concepts and architecture of MAPI.</span></span> 
    
- <span data-ttu-id="64b58-135">[MAPI リファレンス](mapi-reference.md): MAPI の関数、インターフェイス、構造体、プロパティに関する詳細な情報を示します。</span><span class="sxs-lookup"><span data-stu-id="64b58-135">[MAPI Reference](mapi-reference.md) - Provides detailed information about the functions, interfaces, structures, and properties in MAPI.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="64b58-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="64b58-136">See also</span></span>

- [<span data-ttu-id="64b58-137">Outlook MAPI リファレンスの概要</span><span class="sxs-lookup"><span data-stu-id="64b58-137">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)
- [<span data-ttu-id="64b58-138">MAPI のサンプル</span><span class="sxs-lookup"><span data-stu-id="64b58-138">MAPI Samples</span></span>](mapi-samples.md)
- [<span data-ttu-id="64b58-139">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="64b58-139">MAPI Concepts</span></span>](mapi-concepts.md)

