---
title: Outlook ソーシャル コネクタ、プロバイダーの開発の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: Outlook ソーシャル コネクタ (OSC) プロバイダーの参照では、OSC プロバイダーの拡張機能を使用して、OSC プロバイダーを開発する方法について説明します。
ms.openlocfilehash: 19f5ffe8987d0b19017692ddb8f7888be2140033
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804325"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="613d4-103">Outlook ソーシャル コネクタ、プロバイダーの開発の概要</span><span class="sxs-lookup"><span data-stu-id="613d4-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="613d4-104">Outlook ソーシャル コネクタ (OSC) プロバイダーの参照では、OSC プロバイダーの拡張機能を使用して、OSC プロバイダーを開発する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="613d4-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="613d4-105">Outlook のソリューション開発に慣れていない場合、「[Selecting an API or Technology for Developing Outlook Solutions](http://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx)」をご覧になり、ご自身の必要に最も適した API とテクノロジを識別してください。</span><span class="sxs-lookup"><span data-stu-id="613d4-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](http://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="613d4-106">このセクションでは、OSC は、OSC プロバイダーとプロバイダー、技術要件、ベスト ・ プラクティス、プロバイダーを開発するための開発方法の学習の便利なクイック ステップは、どのように、このリリースの新機能の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="613d4-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="613d4-107">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="613d4-107">In this section</span></span>

- <span data-ttu-id="613d4-108">[プロバイダーの新](what-s-new-for-providers.md): OSC の比較は以前のバージョンと現在のリリースでは機能し、インターフェイスのメンバーと追加、変更、またはこのリリースで廃止されている XML スキーマ要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="613d4-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="613d4-109">[Outlook ソーシャル コネクタ プロバイダーを開発する理由](why-develop-an-outlook-social-connector-provider.md): OSC プロバイダーを一般的なソーシャル ネットワーク サイトおよびその他の内部ネットワークのツールは役に立つ方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="613d4-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="613d4-110">[関連する Outlook とソーシャル ネットワークと OSC](relating-the-osc-with-outlook-and-social-networks.md): OSC の Outlook ユーザーのソーシャル ネットワークに接続する方法の構造的なビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="613d4-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="613d4-111">方法を定義する一般的な用語、「ソーシャル ネットワーク」のように [フレンド]、[フレンド以外、] および [連絡先] は、この参照の残りの部分で使用されます。</span><span class="sxs-lookup"><span data-stu-id="613d4-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="613d4-112">[プロバイダーを開発する学習のためのクイック ステップ](quick-steps-for-learning-to-develop-a-provider.md): OSC プロバイダーを開発する方法を説明する手順の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="613d4-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="613d4-113">[技術要件](technical-requirements.md): サポートされているプログラミング言語、COM の可視性の要件、メソッドの戻り値の型の要件、および OSC プロバイダーの拡張機能 DLL の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="613d4-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="613d4-114">[プロバイダーを開発するためのベスト ・ プラクティス](best-practices-for-developing-a-provider.md): OSC プロバイダーを開発する際に、次のベスト プラクティスの一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="613d4-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="613d4-115">リファレンス</span><span class="sxs-lookup"><span data-stu-id="613d4-115">Reference</span></span>

- [<span data-ttu-id="613d4-116">Outlook ソーシャル コネクタ プロバイダーの参照</span><span class="sxs-lookup"><span data-stu-id="613d4-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="613d4-117">関連情報</span><span class="sxs-lookup"><span data-stu-id="613d4-117">Related sections</span></span>

- [<span data-ttu-id="613d4-118">OSC サンプル テンプレート</span><span class="sxs-lookup"><span data-stu-id="613d4-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="613d4-119">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="613d4-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="613d4-120">OSC の XML スキーマを使用してプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="613d4-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="613d4-121">プロバイダーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="613d4-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="613d4-122">プロバイダーを展開します。</span><span class="sxs-lookup"><span data-stu-id="613d4-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="613d4-123">OSC プロバイダーをリリースする準備をします。</span><span class="sxs-lookup"><span data-stu-id="613d4-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="613d4-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="613d4-124">See also</span></span>

- [<span data-ttu-id="613d4-125">Microsoft Outlook ソーシャル コネクタ 32 ビット</span><span class="sxs-lookup"><span data-stu-id="613d4-125">Microsoft Outlook Social Connector 32-bit</span></span>](http://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="613d4-126">Outlook ソーシャル コネクタ (KB983403)、32 ビット版用の更新プログラム</span><span class="sxs-lookup"><span data-stu-id="613d4-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](http://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="613d4-127">Outlook ソーシャル コネクタ (KB983403)、64 ビット版用の更新プログラム</span><span class="sxs-lookup"><span data-stu-id="613d4-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](http://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="613d4-128">Outlook ソーシャル コネクタ 2013: プロバイダー テンプレート</span><span class="sxs-lookup"><span data-stu-id="613d4-128">Outlook Social Connector 2013: Provider templates</span></span>](http://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

