---
title: InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを開発する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- form templates [infopath 2007], using infopath 2003 object model,InfoPath 2003-compatible form templates,InfoPath 2007, developing form templates using InfoPath 2003 object model,object models [InfoPath 2003], developing managed code form templates
localization_priority: Normal
ms.assetid: c74cbcd0-4fe6-4eb7-a05c-f61e1868c42b
description: Microsoft InfoPath は引き続き、Microsoft Office InfoPath 2003 Toolkit for Visual Studio .NET または Visual Studio 2005 Tools for the Microsoft Office system で作成され、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間のメンバーに対して書かれたビジネス ロジックを持つ、フォーム テンプレート プロジェクトをサポートします。このセクションのトピックでは、この名前空間の型とメンバーを InfoPath 2003 互換オブジェクト モデル、または単に InfoPath 2003 オブジェクト モデルと呼びます。InfoPath は、InfoPath 2003 互換オブジェクト モデルを使用する Microsoft Office InfoPath 2007 で作成されたフォーム テンプレート プロジェクトもサポートします。さらに、Office InfoPath 2007 のユーザー向けに下位互換性を維持するため、InfoPath を使用して、InfoPath 2003 互換オブジェクト モデルを使用する新しいフォーム テンプレート プロジェクトを作成できます。このセクションのトピックには、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間によって提供される InfoPath 2003 互換オブジェクト モデルで動作するフォーム テンプレートの作成と開発に固有の情報が記載されています。
ms.openlocfilehash: a39f921f6c7465dbcf469062b866c808fa222851
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401413"
---
# <a name="developing-form-templates-using-the-infopath-2003-object-model"></a><span data-ttu-id="2f268-108">InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを開発する</span><span class="sxs-lookup"><span data-stu-id="2f268-108">Developing Form Templates Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="2f268-p102">Microsoft InfoPath は引き続き、Microsoft Office InfoPath 2003 Toolkit for Visual Studio .NET または Visual Studio 2005 Tools for the Microsoft Office system で作成され、[Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間のメンバーに対して書かれたビジネス ロジックを持つ、フォーム テンプレート プロジェクトをサポートします。このセクションのトピックでは、この名前空間の型とメンバーを InfoPath 2003 互換オブジェクト モデル、または単に InfoPath 2003 オブジェクト モデルと呼びます。InfoPath は、InfoPath 2003 互換オブジェクト モデルを使用する Microsoft Office InfoPath 2007 で作成されたフォーム テンプレート プロジェクトもサポートします。さらに、Office InfoPath 2007 のユーザー向けに下位互換性を維持するため、InfoPath を使用して、InfoPath 2003 互換オブジェクト モデルを使用する新しいフォーム テンプレート プロジェクトを作成できます。このセクションのトピックには、 [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間によって提供される InfoPath 2003 互換オブジェクト モデルで動作するフォーム テンプレートの作成と開発に固有の情報が記載されています。</span><span class="sxs-lookup"><span data-stu-id="2f268-p102">Microsoft InfoPath continues to support form template projects created with Microsoft Office InfoPath 2003 Toolkit for Visual Studio .NET or Visual Studio 2005 Tools for the Microsoft Office System that have business logic written against members of the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace. The topics in this section refer to the types and members of this namespace as the InfoPath 2003-compatible object model or simply the InfoPath 2003 object model. InfoPath also supports form template projects created with Microsoft Office InfoPath 2007 that use the InfoPath 2003-compatible object model. In addition, you can use InfoPath to create new form template projects that use InfoPath 2003-compatible object model to retain backward compatibility for users of Office InfoPath 2007. All topics in this section are specific to creating and developing form templates that work with the InfoPath 2003-compatible object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2f268-p103">[!重要] [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間によって提供されるマネージ コード オブジェクト モデルを使用したビジネス ロジックの作成は今も InfoPath でサポートされていますが、このオブジェクト モデルを使用して書かれたビジネス ロジックは、InfoPath Forms Services を実行する Microsoft SharePoint Server 2010 に展開されたブラウザー対応のフォーム テンプレートではサポートされていません。ブラウザー対応フォーム テンプレートは、カスタム ビジネス ロジック用に、 [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間のメンバーによって提供される新しい InfoPath マネージ コード オブジェクト モデルを使用する必要があります。 [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間のメンバーを使用して書かれたビジネス ロジックでフォーム テンプレートを作成する方法の詳細については、「 [コードを含む InfoPath フォーム テンプレートを開発する](developing-infopath-form-templates-with-code.md)」を参照してください。 > Visual Studio 2012 でコンパイルされたフォーム テンプレートのユーザーのコンピューターには、Microsoft .NET Framework 2.0 またはそれ以降がインストールされている必要があります。Visual Studio .NET 2003 でコンパイルされたフォーム テンプレートのユーザーのコンピューターには、Microsoft .NET Framework 1.1 があればかまいません。</span><span class="sxs-lookup"><span data-stu-id="2f268-p103">Although creating business logic with the managed-code object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace is still supported by InfoPath, business logic written using this object model it is not supported for browser-enabled form templates deployed to Microsoft SharePoint Server 2010 with InfoPath Forms Services. Browser-enabled form templates must use the new InfoPath managed code object model provided by members of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace for custom business logic. For more information about creating form templates with business logic written with members of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace, see [Developing InfoPath Form Templates with Code](developing-infopath-form-templates-with-code.md). > Also, note that users of form templates compiled with Visual Studio 2012 must have Microsoft .NET Framework 2.0 or later installed on their computers. Users of form templates compiled with Visual Studio .NET 2003 are only required to have Microsoft .NET Framework 1.1 on their computers.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="2f268-119">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="2f268-119">In this section</span></span>

[<span data-ttu-id="2f268-120">InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートの開発作業を開始する</span><span class="sxs-lookup"><span data-stu-id="2f268-120">Getting Started Developing Form Templates Using the InfoPath 2003 Object Model</span></span>](get-started-developing-form-templates-using-infopath-object-model.md)
  
> <span data-ttu-id="2f268-121">InfoPath 2003 互換オブジェクト モデルで動作するマネージ コード フォーム テンプレートの作成を開始する方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="2f268-121">Provides information about how to start creating managed code form templates that work with the InfoPath 2003-compatible object model.</span></span>
    
[<span data-ttu-id="2f268-122">InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="2f268-122">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>](creating-form-templates-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="2f268-123">初期化とクリーンアップ コード、イベント ハンドラーの追加方法、マネージ コード フォーム テンプレートのデバッグと展開方法、スレッドのサポート、および InfoPath マネージ コード ソリューションから Microsoft XML Core Services (MSXML) で作業する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f268-123">Discusses initialization and clean-up code, how to add event handlers, how to debug and deploy managed-code form templates, threading support, and working with Microsoft XML Core Services (MSXML) from InfoPath managed-code solutions.</span></span>
    
[<span data-ttu-id="2f268-124">コードを含む InfoPath フォーム テンプレートのセキュリティ</span><span class="sxs-lookup"><span data-stu-id="2f268-124">Security in InfoPath Form Templates with Code</span></span>](security-in-infopath-form-templates-with-code.md)
  
> <span data-ttu-id="2f268-125">マネージ コードを使用した InfoPath フォーム テンプレートのセキュリティ モデル、完全に信頼された InfoPath フォーム テンプレートのデバッグ、および関連するセキュリティ手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f268-125">Discusses the security model for InfoPath form templates that use managed code, debugging fully-trusted InfoPath form templates, and related security procedures.</span></span>
    
[<span data-ttu-id="2f268-126">InfoPath 2003 オブジェクト モデルを理解する</span><span class="sxs-lookup"><span data-stu-id="2f268-126">Understanding the InfoPath 2003 Object Model</span></span>](understanding-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="2f268-127">InfoPath 2003 互換オブジェクト モデル、およびそのオブジェクト モデルで動作するマネージ コード フォーム テンプレートのプログラミングでよく行う作業について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f268-127">Discusses the InfoPath 2003-compatible object model, and common programming tasks for managed code form templates that work with that object model.</span></span>
    
[<span data-ttu-id="2f268-128">InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレートをトラブルシューティングする</span><span class="sxs-lookup"><span data-stu-id="2f268-128">Troubleshooting Form Templates That Use the InfoPath 2003 Object Model</span></span>](troubleshoot-form-templates-that-use-infopath-object-model.md)
  
> <span data-ttu-id="2f268-129">InfoPath 2003 互換オブジェクト モデルで動作するマネージ コード フォーム テンプレートを作成する際に発生する可能性のある一般的な問題の解決に役立つヒントが記載されています。</span><span class="sxs-lookup"><span data-stu-id="2f268-129">Contains tips for solving common problems that you might encounter when creating managed-code form templates that work with the InfoPath 2003-compatible object model.</span></span>
    
## <a name="related-sections"></a><span data-ttu-id="2f268-130">関連情報</span><span class="sxs-lookup"><span data-stu-id="2f268-130">Related sections</span></span>

[<span data-ttu-id="2f268-131">InfoPath デベロッパー ポータル</span><span class="sxs-lookup"><span data-stu-id="2f268-131">InfoPath Developer Portal</span></span>](https://go.microsoft.com/fwlink?LinkID=11689)
  
> <span data-ttu-id="2f268-132">カスタム InfoPath ソリューションの構築に関する技術的な記事、コード サンプル、ダウンロード、サポート、およびその他の MSDN ドキュメントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f268-132">Contains links to technical articles, code samples, downloads, support, and other MSDN documentation on building custom InfoPath solutions.</span></span>
    
[<span data-ttu-id="2f268-133">Microsoft Office デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="2f268-133">Microsoft Office Developer Center</span></span>](https://go.microsoft.com/fwlink?LinkID=27128)
  
> <span data-ttu-id="2f268-134">カスタム Office ソリューションの構築に関する技術的な記事、コード サンプル、ダウンロード、サポート、およびその他の MSDN ドキュメントへのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f268-134">Contains links to technical articles, code samples, downloads, support, and other MSDN documentation on building custom Office solutions.</span></span>
    

