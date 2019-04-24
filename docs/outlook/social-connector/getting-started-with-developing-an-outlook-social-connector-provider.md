---
title: Outlook Social Connector プロバイダーの開発の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: Outlook Social Connector (.osc) プロバイダリファレンスは、.osc プロバイダー拡張機能を使用して、.osc プロバイダーを開発する方法について説明します。
ms.openlocfilehash: 24f8eabe33103f53e848f055b72fd402bc5dd89a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327161"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="d2bdb-103">Outlook Social Connector プロバイダーの開発の概要</span><span class="sxs-lookup"><span data-stu-id="d2bdb-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="d2bdb-104">Outlook Social Connector (.osc) プロバイダリファレンスは、.osc プロバイダー拡張機能を使用して、.osc プロバイダーを開発する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="d2bdb-105">Outlook のソリューション開発に慣れていない場合、「[Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx)」をご覧になり、ご自身の必要に最も適した API とテクノロジを識別してください。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="d2bdb-106">このセクションでは、.osc の概要、.osc プロバイダーが役に立つ方法、プロバイダーの開発方法、技術要件、プロバイダーを開発するためのベストプラクティス、およびこのリリースの新機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="d2bdb-107">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="d2bdb-107">In this section</span></span>

- <span data-ttu-id="d2bdb-108">[プロバイダーの新](what-s-new-for-providers.md)機能: 以前のリリースと現在のリリースの .osc 機能を比較し、このリリースで追加、変更、または廃止されたインターフェイスメンバーと XML スキーマ要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="d2bdb-109">[Outlook Social Connector プロバイダーを開発する理由](why-develop-an-outlook-social-connector-provider.md): .osc プロバイダーが、一般的なソーシャルネットワークサイトやその他の内部ネットワークツールでどのように役立つかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="d2bdb-110">[.osc と outlook およびソーシャルネットワークと](relating-the-osc-with-outlook-and-social-networks.md)の関係: この例では、.osc が outlook ユーザーとソーシャルネットワークを接続する方法についてのアーキテクチャビューを示します。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="d2bdb-111">また、このリファレンスの残りの部分では、「ソーシャルネットワーク」、「友人」、「友人以外」、「連絡先」などの一般的な用語を使用する方法も定義します。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="d2bdb-112">[プロバイダーを開発するための簡単な手順](quick-steps-for-learning-to-develop-a-provider.md): タスクの概要について説明します。この概要では、.osc プロバイダーを開発する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="d2bdb-113">[技術要件](technical-requirements.md): サポートされているプログラミング言語、COM の可視性の要件、メソッドの戻り値の型の要件、および .osc プロバイダ拡張 DLL の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="d2bdb-114">[プロバイダーを開発するためのベストプラクティス](best-practices-for-developing-a-provider.md): .osc プロバイダーの開発時に従うベストプラクティスの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="d2bdb-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="d2bdb-115">リファレンス</span><span class="sxs-lookup"><span data-stu-id="d2bdb-115">Reference</span></span>

- [<span data-ttu-id="d2bdb-116">Outlook Social Connector プロバイダーリファレンス</span><span class="sxs-lookup"><span data-stu-id="d2bdb-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="d2bdb-117">関連情報</span><span class="sxs-lookup"><span data-stu-id="d2bdb-117">Related sections</span></span>

- [<span data-ttu-id="d2bdb-118">.osc サンプルテンプレート</span><span class="sxs-lookup"><span data-stu-id="d2bdb-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="d2bdb-119">通常の呼び出しシーケンスの .osc</span><span class="sxs-lookup"><span data-stu-id="d2bdb-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="d2bdb-120">.osc XML スキーマを使用してプロバイダーを開発する</span><span class="sxs-lookup"><span data-stu-id="d2bdb-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="d2bdb-121">プロバイダーをデバッグする</span><span class="sxs-lookup"><span data-stu-id="d2bdb-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="d2bdb-122">プロバイダーを展開する</span><span class="sxs-lookup"><span data-stu-id="d2bdb-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="d2bdb-123">.osc プロバイダーをリリースする準備をする</span><span class="sxs-lookup"><span data-stu-id="d2bdb-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="d2bdb-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2bdb-124">See also</span></span>

- [<span data-ttu-id="d2bdb-125">Microsoft Outlook Social Connector 32 ビット</span><span class="sxs-lookup"><span data-stu-id="d2bdb-125">Microsoft Outlook Social Connector 32-bit</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="d2bdb-126">Outlook Social Connector (KB983403)、32ビット版の更新プログラム</span><span class="sxs-lookup"><span data-stu-id="d2bdb-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="d2bdb-127">Outlook Social Connector (KB983403)、64ビット版の更新プログラム</span><span class="sxs-lookup"><span data-stu-id="d2bdb-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="d2bdb-128">Outlook Social Connector 2013: プロバイダーテンプレート</span><span class="sxs-lookup"><span data-stu-id="d2bdb-128">Outlook Social Connector 2013: Provider templates</span></span>](https://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

