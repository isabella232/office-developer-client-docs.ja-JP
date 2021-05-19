---
title: Project Server ワークフロー開発の作業開始
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Project Server 2013 の需要管理プロセスには、プロジェクト提案とポートフォリオ分析の管理に役立つワークフローが含まれます。 ここでは、Project Server のワークフローを作成する方法について説明します。
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344472"
---
# <a name="getting-started-developing-project-server-workflows"></a><span data-ttu-id="cfeb9-104">Project Server ワークフロー開発の作業開始</span><span class="sxs-lookup"><span data-stu-id="cfeb9-104">Getting started developing Project Server workflows</span></span>

<span data-ttu-id="cfeb9-105">Project Server 2013 の需要管理プロセスには、プロジェクト提案とポートフォリオ分析の管理に役立つワークフローが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cfeb9-105">Demand management processes in Project Server 2013 include workflows that help you manage project proposals and portfolio analyses.</span></span> <span data-ttu-id="cfeb9-106">ここでは、Project Server のワークフローを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cfeb9-106">This section includes articles that show how to create workflows for Project Server.</span></span>
  
<span data-ttu-id="cfeb9-107">ProjectServer 2013 ワークフローでは、SharePoint Server 2013 ワークフロー プラットフォームを使用します。これは、Windows ワークフローファンデーション (WF4) のバージョン 4 で構築されています。</span><span class="sxs-lookup"><span data-stu-id="cfeb9-107">Project Server 2013 workflows use the SharePoint Server 2013 workflow platform, which is built on version 4 of Windows Workflow Foundation (WF4).</span></span> <span data-ttu-id="cfeb9-108">WF4 ベースのワークフローは宣言型であり、ワークフロー設計ツールはワークフロー ステージ、アクション、条件、その他の要素を XAML コードに保存し、実行時に解釈されます。</span><span class="sxs-lookup"><span data-stu-id="cfeb9-108">WF4-based workflows are declarative, which means that the workflow design tool saves workflow stages, actions, conditions, and other elements to XAML code, which is interpreted at run-time.</span></span> <span data-ttu-id="cfeb9-109">宣言型ワークフローを作成SharePointデザイナー 2013 または 2012 Visual Studioを使用できます。</span><span class="sxs-lookup"><span data-stu-id="cfeb9-109">You can use either SharePoint Designer 2013 or Visual Studio 2012 to create declarative workflows.</span></span> <span data-ttu-id="cfeb9-110">ワークフローには、ワークフロー マネージャー クライアント 1.0 実行エンジンが必要です。これは、オンプレミス ソリューションのローカル サーバー上に、または Project Online ソリューション用のリモート サーバー上にある場合があります。</span><span class="sxs-lookup"><span data-stu-id="cfeb9-110">A workflow requires the Workflow Manager Client 1.0 execution engine, which can be on a local server for on-premises solutions or on a remote server for Project Online solutions.</span></span>
  
<span data-ttu-id="cfeb9-111">デザイナー 2013 SharePoint使用して、比較的単純な宣言型ワークフローを作成できます。</span><span class="sxs-lookup"><span data-stu-id="cfeb9-111">You can use SharePoint Designer 2013 to create relatively simple declarative workflows.</span></span> <span data-ttu-id="cfeb9-112">複雑なワークフローと再利用できるワークフロー テンプレートの場合は、Visual Studio 2012 を使用して、Project Web App のワークフローを開発およびデバッグできます。</span><span class="sxs-lookup"><span data-stu-id="cfeb9-112">For complex workflows, and workflow templates that can be reused, you can use Visual Studio 2012 to develop and debug workflows for Project Web App.</span></span> <span data-ttu-id="cfeb9-113">詳細については[、「2012 年 2012 年を使用Projectワークフローの作成Visual Studio参照してください](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)。</span><span class="sxs-lookup"><span data-stu-id="cfeb9-113">For more information, see [Creating Project Workflows using Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="cfeb9-114">ワークフローを開発およびテストするには、Projectサーバーのテスト インストールを使用します。</span><span class="sxs-lookup"><span data-stu-id="cfeb9-114">Use a test installation of Project Server, not a production installation, to develop and test workflows.</span></span> <span data-ttu-id="cfeb9-115">Project Server 2013 のプレリリース バージョン用に開発されたワークフローは、リリース バージョンについてテストする必要があります。また、再度作成して再展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfeb9-115">Workflows that are developed for pre-release versions of Project Server 2013 must be tested for the release version, and may have to be created again and redeployed.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="cfeb9-116">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="cfeb9-116">In this section</span></span>

[<span data-ttu-id="cfeb9-117">需要管理Projectサーバー ワークフローを作成する</span><span class="sxs-lookup"><span data-stu-id="cfeb9-117">Create a Project Server workflow for Demand Management</span></span>](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a><span data-ttu-id="cfeb9-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="cfeb9-118">See also</span></span>



[<span data-ttu-id="cfeb9-119">カスタム フィールドを一括更新し、プロジェクト サイトをワークフローからProject Onlineする</span><span class="sxs-lookup"><span data-stu-id="cfeb9-119">Bulk update custom fields and create project sites from a Project Online workflow</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[<span data-ttu-id="cfeb9-120">SharePoint Designer 2013 および Visio 2013 でのワークフロー開発</span><span class="sxs-lookup"><span data-stu-id="cfeb9-120">Workflow development in SharePoint Designer 2013 and Visio 2013</span></span>](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[<span data-ttu-id="cfeb9-121">SharePoint ワークフローの新機能</span><span class="sxs-lookup"><span data-stu-id="cfeb9-121">What's new in workflows for SharePoint 2013</span></span>](https://msdn.microsoft.com/library/jj163177.aspx)
  
[<span data-ttu-id="cfeb9-122">Visual Studio を使用した SharePoint 2013 ワークフローの開発</span><span class="sxs-lookup"><span data-stu-id="cfeb9-122">Develop SharePoint 2013 workflows using Visual Studio</span></span>](https://msdn.microsoft.com/library/jj163199.aspx)
  
[<span data-ttu-id="cfeb9-123">2012 Projectを使用したワークフロー Visual Studio作成</span><span class="sxs-lookup"><span data-stu-id="cfeb9-123">Creating Project Workflows using Visual Studio 2012</span></span>](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[<span data-ttu-id="cfeb9-124">Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="cfeb9-124">Windows Workflow Foundation</span></span>](https://msdn.microsoft.com/library/dd489441.aspx)
  
[<span data-ttu-id="cfeb9-125">開発者による .NET 4 Windowsワークフローファンデーション (WF) の概要</span><span class="sxs-lookup"><span data-stu-id="cfeb9-125">A developer's introduction to Windows Workflow Foundation (WF) in .NET 4</span></span>](https://msdn.microsoft.com/library/ee342461.aspx)
  
[<span data-ttu-id="cfeb9-126">Hitchhiker の需要管理ガイド (ホワイト ペーパー)</span><span class="sxs-lookup"><span data-stu-id="cfeb9-126">Hitchhiker's guide to demand management (white paper)</span></span>](https://msdn.microsoft.com/library/ff973112.aspx)

