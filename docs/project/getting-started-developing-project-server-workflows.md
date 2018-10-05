---
title: Project Server ワークフロー開発の作業開始
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Project Server 2013 の管理プロセスを支援するワークフローを含む要求は、プロジェクトの提案とポートフォリオ分析を管理します。 このセクションには、Project Server のワークフローを作成する方法を説明する記事が含まれています。
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384095"
---
# <a name="getting-started-developing-project-server-workflows"></a><span data-ttu-id="6f28d-104">Project Server ワークフロー開発の作業開始</span><span class="sxs-lookup"><span data-stu-id="6f28d-104">Getting started developing Project Server workflows</span></span>

<span data-ttu-id="6f28d-105">Project Server 2013 の管理プロセスを支援するワークフローを含む要求は、プロジェクトの提案とポートフォリオ分析を管理します。</span><span class="sxs-lookup"><span data-stu-id="6f28d-105">Demand management processes in Project Server 2013 include workflows that help you manage project proposals and portfolio analyses.</span></span> <span data-ttu-id="6f28d-106">このセクションには、Project Server のワークフローを作成する方法を説明する記事が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f28d-106">This section includes articles that show how to create workflows for Project Server.</span></span>
  
<span data-ttu-id="6f28d-107">Project Server 2013 のワークフローでは、Windows ワークフロー Foundation (WF4) のバージョン 4 の上に構築された、SharePoint Server 2013 ワークフロー プラットフォームを使用します。</span><span class="sxs-lookup"><span data-stu-id="6f28d-107">Project Server 2013 workflows use the SharePoint Server 2013 workflow platform, which is built on version 4 of Windows Workflow Foundation (WF4).</span></span> <span data-ttu-id="6f28d-108">WF4 ベースのワークフローは宣言的なワークフローのデザイン ツールで、実行時に解釈されますが、XAML コードをワークフロー ステージ、アクション、条件、およびその他の要素を保存します。</span><span class="sxs-lookup"><span data-stu-id="6f28d-108">WF4-based workflows are declarative, which means that the workflow design tool saves workflow stages, actions, conditions, and other elements to XAML code, which is interpreted at run-time.</span></span> <span data-ttu-id="6f28d-109">宣言型ワークフローを作成するのには、SharePoint Designer 2013 または Visual Studio 2012 のいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6f28d-109">You can use either SharePoint Designer 2013 or Visual Studio 2012 to create declarative workflows.</span></span> <span data-ttu-id="6f28d-110">ワークフローでは、オンプレミスのソリューションのローカル サーバー上またはオンライン プロジェクトのソリューション用のリモート サーバーには、ワークフロー マネージャーのクライアント 1.0 の実行エンジンが必要です。</span><span class="sxs-lookup"><span data-stu-id="6f28d-110">A workflow requires the Workflow Manager Client 1.0 execution engine, which can be on a local server for on-premises solutions or on a remote server for Project Online solutions.</span></span>
  
<span data-ttu-id="6f28d-111">SharePoint Designer 2013 を使用すると、比較的単純な宣言型ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="6f28d-111">You can use SharePoint Designer 2013 to create relatively simple declarative workflows.</span></span> <span data-ttu-id="6f28d-112">複雑なワークフローは、ワークフロー テンプレートを再利用できるを開発し、Project Web App のワークフローをデバッグするのに Visual Studio 2012 を使用できます。</span><span class="sxs-lookup"><span data-stu-id="6f28d-112">For complex workflows, and workflow templates that can be reused, you can use Visual Studio 2012 to develop and debug workflows for Project Web App.</span></span> <span data-ttu-id="6f28d-113">詳細については、[プロジェクトのワークフローを作成する Visual Studio 2012 を使用して](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f28d-113">For more information, see [Creating Project Workflows using Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6f28d-114">作成し、ワークフローをテストするには、実稼働インストールではなく、Project Server のテスト環境を使用します。</span><span class="sxs-lookup"><span data-stu-id="6f28d-114">Use a test installation of Project Server, not a production installation, to develop and test workflows.</span></span> <span data-ttu-id="6f28d-115">Project Server 2013 のプレリリース バージョン用に開発されたワークフローでは、リリース バージョンでは、テストする必要があるし、再作成して再展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f28d-115">Workflows that are developed for pre-release versions of Project Server 2013 must be tested for the release version, and may have to be created again and redeployed.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="6f28d-116">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="6f28d-116">In this section</span></span>

[<span data-ttu-id="6f28d-117">需要管理用の Project Server ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="6f28d-117">Create a Project Server workflow for Demand Management</span></span>](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a><span data-ttu-id="6f28d-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f28d-118">See also</span></span>



[<span data-ttu-id="6f28d-119">更新プログラムのユーザー設定フィールドを一括して、オンラインのプロジェクトのワークフローからプロジェクト サイトを作成</span><span class="sxs-lookup"><span data-stu-id="6f28d-119">Bulk update custom fields and create project sites from a Project Online workflow</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[<span data-ttu-id="6f28d-120">Workflow development in SharePoint Designer 2013 and Visio 2013</span><span class="sxs-lookup"><span data-stu-id="6f28d-120">Workflow development in SharePoint Designer 2013 and Visio 2013</span></span>](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[<span data-ttu-id="6f28d-121">SharePoint ワークフローの新機能</span><span class="sxs-lookup"><span data-stu-id="6f28d-121">What's new in workflows for SharePoint 2013</span></span>](https://msdn.microsoft.com/library/jj163177.aspx)
  
[<span data-ttu-id="6f28d-122">Visual Studio を使用した SharePoint 2013 ワークフローの開発</span><span class="sxs-lookup"><span data-stu-id="6f28d-122">Develop SharePoint 2013 workflows using Visual Studio</span></span>](https://msdn.microsoft.com/library/jj163199.aspx)
  
[<span data-ttu-id="6f28d-123">Visual Studio 2012 を使用してプロジェクトのワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="6f28d-123">Creating Project Workflows using Visual Studio 2012</span></span>](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[<span data-ttu-id="6f28d-124">Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="6f28d-124">Windows Workflow Foundation</span></span>](https://msdn.microsoft.com/library/dd489441.aspx)
  
[<span data-ttu-id="6f28d-125">Windows ワークフロー Foundation (WF) .NET 4 での開発者の概要</span><span class="sxs-lookup"><span data-stu-id="6f28d-125">A developer's introduction to Windows Workflow Foundation (WF) in .NET 4</span></span>](https://msdn.microsoft.com/library/ee342461.aspx)
  
[<span data-ttu-id="6f28d-126">Hitchhiker のガイド需要管理 (ホワイト ペーパー)</span><span class="sxs-lookup"><span data-stu-id="6f28d-126">Hitchhiker's guide to demand management (white paper)</span></span>](https://msdn.microsoft.com/library/ff973112.aspx)

