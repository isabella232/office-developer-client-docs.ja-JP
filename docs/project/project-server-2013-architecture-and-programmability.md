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
- project 2013、アーキテクチャとプログラミング、プログラミング、Project Server、Project 2013、EPM、アーキテクチャ、および Project Server の利点
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: このセクションの記事では、Project Professional 2013、Project Server 2013、Project Web App、および SharePoint Server 2013 を組み合わせたエンタープライズ プロジェクト管理 (EPM) ソリューションの全体的なアーキテクチャについて説明します。
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413788"
---
# <a name="project-server-2013-architecture-and-programmability"></a><span data-ttu-id="56187-104">Project Server 2013 のアーキテクチャおよびプログラミング</span><span class="sxs-lookup"><span data-stu-id="56187-104">Project Server 2013 architecture and programmability</span></span>

<span data-ttu-id="56187-105">このセクションの記事では、Project Professional 2013、Project Server 2013、Project Web App、および SharePoint Server 2013 を組み合わせたエンタープライズ プロジェクト管理 (EPM) ソリューションの全体的なアーキテクチャについて説明します。</span><span class="sxs-lookup"><span data-stu-id="56187-105">The articles in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="56187-106">Project Server 2013は、.NET Framework 4 で構築され、真のマルチティア アーキテクチャを提供する Project Server の 3 番目のメジャー リリースです。</span><span class="sxs-lookup"><span data-stu-id="56187-106">Project Server 2013 is built with the .NET Framework 4 and is the third major release of Project Server to provide a true multitier architecture.</span></span> <span data-ttu-id="56187-107">クラウド アクセスの場合、Project Server 2013 は、Web アプリケーション、モバイル アプリケーション、および Silverlight アプリケーションで使用できるレポート用のクライアント側オブジェクト モデル (CSOM) と OData サービスを実装します。</span><span class="sxs-lookup"><span data-stu-id="56187-107">For cloud access, Project Server 2013 implements a client-side object model (CSOM) and an OData service for reporting that can be used in web applications, mobile applications, and Silverlight applications.</span></span> <span data-ttu-id="56187-108">社内設置型アプリケーションの場合、クライアントは CSOM または Project Server Interface (PSI) サービスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="56187-108">For applications on-premises, clients can use either the CSOM or the Project Server Interface (PSI) services.</span></span> 
  
## <a name="introduction-to-project-server-architecture"></a><span data-ttu-id="56187-109">Project Server アーキテクチャの概要</span><span class="sxs-lookup"><span data-stu-id="56187-109">Introduction to Project Server architecture</span></span>

<span data-ttu-id="56187-110">このセクションのトピックでは、Project Professional 2013、Project Server 2013、Project Web App、および SharePoint Server 2013 を組み合わせたエンタープライズ プロジェクト管理 (EPM) ソリューションの全体的なアーキテクチャについて説明します。</span><span class="sxs-lookup"><span data-stu-id="56187-110">The topics in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="56187-111">Project Server にプログラムでアクセスするには、CSOM または PSI サービスを Windows Communication Foundation (WCF) インターフェイスで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="56187-111">For programmatic access to Project Server, you should use either the CSOM or the PSI services with the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="56187-112">PSI の ASMX Web サービス インターフェイスは、Project Server 2013で使用されていませんが、引き続き機能します。</span><span class="sxs-lookup"><span data-stu-id="56187-112">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but still works.</span></span> <span data-ttu-id="56187-113">PSI はデータセットの使用による効率的なアクセスを可能にし、サーバー側イベントのハンドラーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="56187-113">The PSI enables efficient access by using datasets and you can create handlers for server-side events.</span></span> <span data-ttu-id="56187-114">CSOM 自身は PSI を使用して、Project Server のビジネス オブジェクト層にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="56187-114">The CSOM itself uses the PSI to access the Project Server business object layer.</span></span> <span data-ttu-id="56187-115">4 つの Project Server データベースの代わりに、Project Server 2013アクセス層で 1 つのデータベースを使用します。</span><span class="sxs-lookup"><span data-stu-id="56187-115">Instead of four Project Server databases, Project Server 2013 uses a single database in the data access layer.</span></span>
  
<span data-ttu-id="56187-116">Project Server 2013 SharePoint Server 2013 と深く統合されます。</span><span class="sxs-lookup"><span data-stu-id="56187-116">Project Server 2013 integrates deeply with SharePoint Server 2013.</span></span> <span data-ttu-id="56187-117">Project アプリケーション サービスは、ファーム内の他の SharePoint サイト コレクションに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="56187-117">The Project Application Service can be associated with other SharePoint site collections in the farm.</span></span> <span data-ttu-id="56187-118">Project Server はサイト コレクション内の SharePoint タスク リストを操作し、レポートを生成できるほか、Project Server がタスク リストをエンタープライズ プロジェクトとしてインポートおよび管理する場合に完全に制御することもできます。</span><span class="sxs-lookup"><span data-stu-id="56187-118">Project Server can operate with and report on SharePoint task lists in the site collection, and can also get full control where Project Server imports and manages the task lists as enterprise projects.</span></span> <span data-ttu-id="56187-119">Project Server では、Windows Workflow Foundation (WF4) のバージョン 4 も使用し、需要管理ソリューションのワークフロー アクティビティを追加します。</span><span class="sxs-lookup"><span data-stu-id="56187-119">Project Server also uses version 4 of the Windows Workflow Foundation (WF4) and adds workflow activities for Demand Management solutions.</span></span>
  
<span data-ttu-id="56187-120">Project 2013 が開発者に提供する多くの新機能、および非推奨の機能の詳細については、「Project 2013 の開発者向け [更新プログラム」を参照してください](updates-for-developers-in-project-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="56187-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="56187-121">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="56187-121">In this section</span></span>

<span data-ttu-id="56187-122">[Project Server 2013アーキテクチャでは](project-server-2013-architecture.md) 、クライアントやサーバーなど、Project 2013プラットフォームの主要な部分について説明します。</span><span class="sxs-lookup"><span data-stu-id="56187-122">[Project Server 2013 architecture](project-server-2013-architecture.md) describes the major parts of the Project 2013 platform, including the clients and servers.</span></span> 
  
<span data-ttu-id="56187-123">[Project Server のプログラミングでは](project-server-programmability.md) 、Project Server 2013 の主な機能拡張機能、Project Web App のカスタマイズ、以前の Project Server バージョン用に構築されたアプリケーションのアップグレードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="56187-123">[Project Server programmability](project-server-programmability.md) discusses the main extensibility features of Project Server 2013, customization of Project Web App, and upgrading applications that are built for previous Project Server versions.</span></span> 
  
<span data-ttu-id="56187-124">「[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md)」では、PSI を使用できるシナリオと PSI で実行できない操作について説明します。</span><span class="sxs-lookup"><span data-stu-id="56187-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describes scenarios where the PSI can be used and lists things that the PSI cannot do.</span></span> 
  
<span data-ttu-id="56187-125">「[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md)」では、CSOM を使用できるシナリオと CSOM で実行できない操作について説明します。</span><span class="sxs-lookup"><span data-stu-id="56187-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describes scenarios where the CSOM can be used and lists things that the CSOM cannot do.</span></span> 
  
### <a name="topics-not-covered"></a><span data-ttu-id="56187-126">扱わない内容</span><span class="sxs-lookup"><span data-stu-id="56187-126">Topics not covered</span></span>

<span data-ttu-id="56187-127">「アーキテクチャとプログラミング」  *セクション*  の記事では、Project デスクトップ クライアント (Project Standard 2013 および Project Professional 2013) またはプロジェクト の機能はProject Web App。</span><span class="sxs-lookup"><span data-stu-id="56187-127">The articles in the  *Architecture and programmability*  section do not document features of the Project desktop clients (Project Standard 2013 and Project Professional 2013) or Project Web App.</span></span> 
  
<span data-ttu-id="56187-128">Project Standard および Project Professional 内では、Visual Basic Editor で Visual Basic for Applications (VBA) ヘルプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="56187-128">Visual Basic for Applications (VBA) help is available in the Visual Basic editor within Project Standard and Project Professional.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="56187-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="56187-129">See also</span></span>
<span data-ttu-id="56187-130"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="56187-130"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="56187-131">Project 2013 における開発者向けの更新内容</span><span class="sxs-lookup"><span data-stu-id="56187-131">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md)
    
- [<span data-ttu-id="56187-132">Project Server ワークフロー開発の作業開始</span><span class="sxs-lookup"><span data-stu-id="56187-132">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
    

