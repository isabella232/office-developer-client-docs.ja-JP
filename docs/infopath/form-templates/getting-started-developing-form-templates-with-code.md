---
title: コードを含むフォーム テンプレートの開発作業を開始する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- form templates [infopath 2007], getting started,managed code form templates [InfoPath 2007], getting started,InfoPath 2007, getting started
localization_priority: Normal
ms.assetid: 66468447-2012-4497-b371-c61f64a8bb49
description: ここでは、Microsoft.Office.InfoPath 名前空間のメンバーから提供される InfoPath オブジェクト モデルを使用するマネージ コード フォーム テンプレートを作成する作業の始め方を説明します。
ms.openlocfilehash: a4e4e8a4e01dc8d0fbfe9c5cbed0ae4b85b51e94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19799111"
---
# <a name="getting-started-developing-form-templates-with-code"></a><span data-ttu-id="376d3-104">コードを含むフォーム テンプレートの開発作業を開始する</span><span class="sxs-lookup"><span data-stu-id="376d3-104">Getting Started Developing Form Templates with Code</span></span>

<span data-ttu-id="376d3-105">ここでは、 **Microsoft.Office.InfoPath** 名前空間のメンバーから提供される InfoPath オブジェクト モデルを使用するマネージ コード フォーム テンプレートを作成する作業の始め方を説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-105">This section provides information on how to get started creating managed code form templates that work with the InfoPath object model provided by members of the **Microsoft.Office.InfoPath** namespace.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="376d3-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="376d3-106">In this section</span></span>

[<span data-ttu-id="376d3-107">InfoPath 開発者向けの新機能</span><span class="sxs-lookup"><span data-stu-id="376d3-107">What's New for InfoPath Developers</span></span>](what-s-new-for-infopath-developers.md)
  
> <span data-ttu-id="376d3-108">開発者にとって便利な新機能や改良された機能を説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-108">Provides information on new features and improvements that are of interest to developers.</span></span>
    
[<span data-ttu-id="376d3-109">InfoPath のオブジェクト モデルと開発環境を理解する</span><span class="sxs-lookup"><span data-stu-id="376d3-109">Understanding InfoPath Object Models and Development Environment</span></span>](understanding-infopath-object-models-and-development-environment.md)
  
> <span data-ttu-id="376d3-110">フォーム テンプレートでのビジネス ロジック開発用の 2 種類のプログラミング モデル、および InfoPath でサポートされる Visual Studio 2012 開発環境について説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-110">Describes the two kinds of programming models for developing business logic in form templates, and the Visual Studio 2012 development environment supported by InfoPath.</span></span>
    
[<span data-ttu-id="376d3-111">Visual Studio で開発する</span><span class="sxs-lookup"><span data-stu-id="376d3-111">How to: Develop with Visual Studio</span></span>](how-to-develop-with-visual-studio.md)
  
> <span data-ttu-id="376d3-112">Visual Studio 2012 環境をインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-112">Describes how to install the Visual Studio 2012 environment.</span></span>
    
[<span data-ttu-id="376d3-113">Visual Studio Tools for Applications の .NET Framework ヘルプをローカルにインストールする</span><span class="sxs-lookup"><span data-stu-id="376d3-113">How to: Install Local .NET Framework Help for Visual Studio Tools for Applications</span></span>](how-to-install-net-framework-help-for-visual-studio-tools-for-applications.md)
  
> <span data-ttu-id="376d3-114">Visual Studio 2012 環境でオフラインで使用するために .NET Framework ドキュメントのローカル コピーをインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-114">Describes how to install a local copy of the .NET Framework documentation for offline use in the Visual Studio 2012 environment.</span></span>
    
[<span data-ttu-id="376d3-115">イベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="376d3-115">Add an Event Handler?</span></span>](how-to-add-an-event-handler.md)
  
> <span data-ttu-id="376d3-116">InfoPath マネージ コード フォーム テンプレートにイベント ハンドラーを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-116">Describes how to add event handlers to an InfoPath managed code form template.</span></span> 
    
[<span data-ttu-id="376d3-117">コードを含む InfoPath フォーム テンプレートをプレビューおよびデバッグする</span><span class="sxs-lookup"><span data-stu-id="376d3-117">Preview and Debug InfoPath Form Templates with Code?</span></span>](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
> <span data-ttu-id="376d3-118">InfoPath マネージ コード フォーム テンプレートをプレビューおよびデバッグする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-118">Describes how to preview and debug InfoPath managed code form templates.</span></span>
    
[<span data-ttu-id="376d3-119">完全信頼が必要なフォーム テンプレートをプレビューおよびデバッグする</span><span class="sxs-lookup"><span data-stu-id="376d3-119">How to: Preview and Debug Form Templates that Require Full Trust</span></span>](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
  
> <span data-ttu-id="376d3-120">完全信頼が必要なビジネス ロジックが含まれている InfoPath マネージ コード フォーム テンプレートをプレビューおよびデバッグする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-120">Describes how to preview and debug InfoPath managed code form templates that contain business logic that requires full trust.</span></span>
    
<span data-ttu-id="376d3-121">[[ウォークスルー] コードを含む基本的なフォーム テンプレートを作成する方法](walkthrough-creating-a-basic-form-template-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="376d3-121">[Walkthrough: Creating a Basic Form Template with Code](walkthrough-creating-a-basic-form-template-with-code.md)</span></span>
  
> <span data-ttu-id="376d3-122">基本的な InfoPath マネージ コード フォーム テンプレートの作成とデバッグの概要を説明する段階的なガイド</span><span class="sxs-lookup"><span data-stu-id="376d3-122">A step-by-step guide that provides an introduction to creating and debugging a basic InfoPath managed code form template</span></span> 
    
[<span data-ttu-id="376d3-123">デバッグのために値のログをフィールドに記録する</span><span class="sxs-lookup"><span data-stu-id="376d3-123">How to: Log Values to a Field for Debugging</span></span>](how-to-log-values-to-a-field-for-debugging.md)
  
> <span data-ttu-id="376d3-124">デバッグ情報をログに記録するための複数行フィールドとヘルパー関数を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-124">Describes how to create a multi-line field and a helper function for logging debugging information.</span></span>
    
[<span data-ttu-id="376d3-125">InfoPath Toolkit で作成したフォーム テンプレートを開くか変換する</span><span class="sxs-lookup"><span data-stu-id="376d3-125">Open or Convert a Form Template Created with the InfoPath Toolkit?</span></span>](how-to-open-or-convert-a-form-template-created-with-the-infopath-toolkit.md)
  
> <span data-ttu-id="376d3-126">InfoPath 2003 Toolkit と Visual Studio .NET または InfoPath 2003 Toolkit for Visual Studio 2005 を使用して作成されたマネージ コード フォーム テンプレートを開くか変換する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-126">Describes how to open or convert a managed code form template created with the InfoPath 2003 Toolkit and Visual Studio .NET or the InfoPath 2003 Toolkit for Visual Studio 2005.</span></span>
    
[<span data-ttu-id="376d3-127">コードを含む InfoPath フォーム テンプレートを展開する</span><span class="sxs-lookup"><span data-stu-id="376d3-127">Deploy InfoPath Form Templates with Code?</span></span>](how-to-deploy-infopath-form-templates-with-code.md)
  
> <span data-ttu-id="376d3-128">InfoPath マネージ コード フォーム テンプレートを展開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-128">Describes how to deploy InfoPath managed code form templates.</span></span>
    
<span data-ttu-id="376d3-129">[[方法] コードを含む InfoPath フォーム テンプレートを操作する方法](how-do-iin-infopath-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="376d3-129">[How Do I...In InfoPath Form Templates with Code](how-do-iin-infopath-form-templates-with-code.md)</span></span>
  
> <span data-ttu-id="376d3-130">InfoPath マネージ コード フォーム テンプレートの開発者を対象とした一般的な作業の要約を説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-130">Provides a summary of common tasks for developers of InfoPath managed code form templates.</span></span>
    
[<span data-ttu-id="376d3-131">XPathNavigator クラスおよび XPathNodeIterator クラスを操作する</span><span class="sxs-lookup"><span data-stu-id="376d3-131">How to: Work with the XPathNavigator and XPathNodeIterator Classes</span></span>](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)
  
> <span data-ttu-id="376d3-132">XML データを操作する **XPathNavigator** クラスおよび **XPathNodeIterator** クラスを使用する InfoPath マネージ クラス オブジェクト モデルのメンバーの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-132">Provides a summary of the members of the InfoPath managed code object model that use the **XPathNavigator** and **XPathNodeIterator** classes to work with XML data.</span></span> 
    
[<span data-ttu-id="376d3-133">SharePoint オブジェクト モデルのメンバーを使用する</span><span class="sxs-lookup"><span data-stu-id="376d3-133">How to: Use SharePoint Object Model Members</span></span>](how-to-use-sharepoint-object-model-members.md)
  
> <span data-ttu-id="376d3-134">フォーム コードからオブジェクト モデルに対するコードを作成できるように、Microsoft.SharePoint アセンブリへの参照を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-134">Describes how to create a reference to the Microsoft.SharePoint assembly so that you can write code against its object model from form code.</span></span>
    
[<span data-ttu-id="376d3-135">コードを含むフォームを発行する</span><span class="sxs-lookup"><span data-stu-id="376d3-135">Publishing Forms with Code</span></span>](publishing-forms-with-code.md)
  
> <span data-ttu-id="376d3-136">サンドボックス ソリューションと管理者展開用のソリューションの違いを説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-136">Describes the differences between publishing sandboxed solutions and administrator-deployed solutions.</span></span>
    
[<span data-ttu-id="376d3-137">サンドボックス ソリューションのサンプル</span><span class="sxs-lookup"><span data-stu-id="376d3-137">Sample Sandboxed Solutions</span></span>](sample-sandboxed-solutions.md)
  
> <span data-ttu-id="376d3-138">InfoPath のサンドボックス ソリューションで記述できる 2 つのコード例を説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-138">Provides two examples that show the kind of code that you can write in an InfoPath sandboxed solution.</span></span>
    
[<span data-ttu-id="376d3-139">InfoPath フォーム テンプレート開発者向けのその他のリソース</span><span class="sxs-lookup"><span data-stu-id="376d3-139">Additional Resources for InfoPath Form Template Developers</span></span>](additional-resources-for-infopath-form-template-developers.md)
  
> <span data-ttu-id="376d3-140">InfoPath 開発者向けの追加情報を検索する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="376d3-140">How to find additional sources of information for InfoPath developers.</span></span>
    

