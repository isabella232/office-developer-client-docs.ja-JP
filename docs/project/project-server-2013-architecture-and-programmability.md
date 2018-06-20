---
title: Project Server 2013 のアーキテクチャおよびプログラミング
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- architecture
- platform
- Project
- Project architecture
- Project programmability
- Project Server architecture
- Project Server programmability
keywords:
- プロジェクト 2013、EPM、アーキテクチャ、および Project Server のアーキテクチャおよびプログラミング、プログラミング、サーバーのプロジェクト、Project 2013 の利点
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: このセクションの記事では、エンタープライズ プロジェクト管理 (EPM) ソリューションでは、評価のためのプロジェクトを Project Server 2013、Project Web App では、SharePoint Server 2013 を組み合わせたものの全体的なアーキテクチャについて説明します。
ms.openlocfilehash: 6b5ab94968dbb996a370e0e5abb89813f5e41ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804685"
---
# <a name="project-server-2013-architecture-and-programmability"></a><span data-ttu-id="d3b60-104">Project Server 2013 のアーキテクチャおよびプログラミング</span><span class="sxs-lookup"><span data-stu-id="d3b60-104">Project Server 2013 architecture and programmability</span></span>

<span data-ttu-id="d3b60-105">このセクションの記事では、エンタープライズ プロジェクト管理 (EPM) ソリューションでは、評価のためのプロジェクトを Project Server 2013、Project Web App では、SharePoint Server 2013 を組み合わせたものの全体的なアーキテクチャについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d3b60-105">The articles in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="d3b60-106">Project Server 2013 は、.NET Framework 4 で作成された、真の多階層アーキテクチャを提供するのには Project Server の 3 番目のメジャー リリースです。</span><span class="sxs-lookup"><span data-stu-id="d3b60-106">Project Server 2013 is built with the .NET Framework 4 and is the third major release of Project Server to provide a true multitier architecture.</span></span> <span data-ttu-id="d3b60-107">クラウドへのアクセスの Project Server 2013 は、web アプリケーション、モバイル アプリケーション、および Silverlight アプリケーションでクライアント側オブジェクト モデル (CSOM) とレポート作成のために使用できる OData サービスを実装します。</span><span class="sxs-lookup"><span data-stu-id="d3b60-107">For cloud access, Project Server 2013 implements a client-side object model (CSOM) and an OData service for reporting that can be used in web applications, mobile applications, and Silverlight applications.</span></span> <span data-ttu-id="d3b60-108">設置型のアプリケーションでは、クライアントは、CSOM またはプロジェクト Server インターフェイス (PSI) のサービスのいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3b60-108">For applications on-premises, clients can use either the CSOM or the Project Server Interface (PSI) services.</span></span> 
  
## <a name="introduction-to-project-server-architecture"></a><span data-ttu-id="d3b60-109">Project Server アーキテクチャの概要</span><span class="sxs-lookup"><span data-stu-id="d3b60-109">Introduction to Project Server architecture</span></span>

<span data-ttu-id="d3b60-110">このセクションのトピックでは、エンタープライズ プロジェクト管理 (EPM) ソリューションでは、評価のためのプロジェクトを Project Server 2013、Project Web App では、SharePoint Server 2013 を組み合わせたものの全体的なアーキテクチャについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d3b60-110">The topics in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="d3b60-111">Project Server にプログラムによるアクセスは、Windows Communication Foundation (WCF) インターフェイスを使用して、CSOM または PSI サービスのいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3b60-111">For programmatic access to Project Server, you should use either the CSOM or the PSI services with the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="d3b60-112">PSI の ASMX web サービスのインタ フェースは、Project Server 2013 のでは使用されなくなりましたは引き続き機能します。</span><span class="sxs-lookup"><span data-stu-id="d3b60-112">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but still works.</span></span> <span data-ttu-id="d3b60-113">PSI は、データセットを使用して、効率的なアクセスを有効にし、サーバー側イベントのハンドラーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d3b60-113">The PSI enables efficient access by using datasets and you can create handlers for server-side events.</span></span> <span data-ttu-id="d3b60-114">自体 CSOM は、Project Server のビジネス オブジェクト層にアクセスするのには、PSI を使用します。</span><span class="sxs-lookup"><span data-stu-id="d3b60-114">The CSOM itself uses the PSI to access the Project Server business object layer.</span></span> <span data-ttu-id="d3b60-115">4 つの Project Server データベースの代わりには、Project Server 2013 は、データ アクセス層で 1 つのデータベースを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3b60-115">Instead of four Project Server databases, Project Server 2013 uses a single database in the data access layer.</span></span>
  
<span data-ttu-id="d3b60-116">Project Server 2013 は、SharePoint Server 2013 で緊密に統合されています。</span><span class="sxs-lookup"><span data-stu-id="d3b60-116">Project Server 2013 integrates deeply with SharePoint Server 2013.</span></span> <span data-ttu-id="d3b60-117">Project アプリケーション サービスは、ファーム内の他の SharePoint サイト コレクションに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d3b60-117">The Project Application Service can be associated with other SharePoint site collections in the farm.</span></span> <span data-ttu-id="d3b60-118">Project Server で動作でき、レポートでは、サイト コレクションでは、タスク ・ リストも、Project Server のインポートし、管理、フル コントロールを取得する SharePoint のエンタープライズ プロジェクトのタスク一覧を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="d3b60-118">Project Server can operate with and report on SharePoint task lists in the site collection, and can also get full control where Project Server imports and manages the task lists as enterprise projects.</span></span> <span data-ttu-id="d3b60-119">Project Server は、Windows ワークフロー Foundation (WF4) のバージョン 4 を使用してもと需要管理ソリューションのワークフロー アクティビティを追加します。</span><span class="sxs-lookup"><span data-stu-id="d3b60-119">Project Server also uses version 4 of the Windows Workflow Foundation (WF4) and adds workflow activities for Demand Management solutions.</span></span>
  
<span data-ttu-id="d3b60-120">開発者は、Project 2013 が提供する多くの新機能と廃止される機能については、 [Project 2013 の開発者用の更新プログラム](updates-for-developers-in-project-2013.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3b60-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="d3b60-121">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="d3b60-121">In this section</span></span>

<span data-ttu-id="d3b60-122">[Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)では、クライアントとサーバーを含む、Project 2013 のプラットフォームの主要な部分について説明します。</span><span class="sxs-lookup"><span data-stu-id="d3b60-122">[Project Server 2013 architecture](project-server-2013-architecture.md) describes the major parts of the Project 2013 platform, including the clients and servers.</span></span> 
  
<span data-ttu-id="d3b60-123">[Project Server プログラミング](project-server-programmability.md)では、Project Server 2013、Project Web App では、Project Server の以前のバージョン用に構築されたアプリケーションのアップグレードのカスタマイズの主要な拡張機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d3b60-123">[Project Server programmability](project-server-programmability.md) discusses the main extensibility features of Project Server 2013, customization of Project Web App, and upgrading applications that are built for previous Project Server versions.</span></span> 
  
<span data-ttu-id="d3b60-124">[何の PSI は行われない](what-the-psi-does-and-does-not-do.md)、PSI を使用できるシナリオについて説明し、PSI を実行できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="d3b60-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describes scenarios where the PSI can be used and lists things that the PSI cannot do.</span></span> 
  
<span data-ttu-id="d3b60-125">[どのような「CSOM が行われない](what-the-csom-does-and-does-not-do.md)CSOM を使用できるシナリオについて説明します CSOM を実行できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="d3b60-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describes scenarios where the CSOM can be used and lists things that the CSOM cannot do.</span></span> 
  
### <a name="topics-not-covered"></a><span data-ttu-id="d3b60-126">扱わない内容</span><span class="sxs-lookup"><span data-stu-id="d3b60-126">Topics not covered</span></span>

<span data-ttu-id="d3b60-127">*アーキテクチャおよびプログラミング*のセクションの記事には、デスクトップ クライアントを (プロジェクトの標準的な 2013 および評価のためのプロジェクト) は、プロジェクトまたは Project Web App の機能は文書化されません。</span><span class="sxs-lookup"><span data-stu-id="d3b60-127">The articles in the  *Architecture and programmability*  section do not document features of the Project desktop clients (Project Standard 2013 and Project Professional 2013) or Project Web App.</span></span> 
  
<span data-ttu-id="d3b60-128">Project Standard および Project Professional 内では、Visual Basic Editor で Visual Basic for Applications (VBA) ヘルプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3b60-128">Visual Basic for Applications (VBA) help is available in the Visual Basic editor within Project Standard and Project Professional.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d3b60-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="d3b60-129">See also</span></span>
<span data-ttu-id="d3b60-130"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="d3b60-130"></span></span>

- [<span data-ttu-id="d3b60-131">Project 2013 の開発者用の更新プログラム</span><span class="sxs-lookup"><span data-stu-id="d3b60-131">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md)
    
- [<span data-ttu-id="d3b60-132">開発 Project Server ワークフローの開始を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3b60-132">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
    

