---
title: InfoPath オブジェクトモデルを使用してフォームテンプレートの開発を開始する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- form templates [infopath 2007], getting started,InfoPath 2003-compatible form templates, getting started
localization_priority: Normal
ms.assetid: 45867711-3231-43ce-bae9-caf588120550
description: ここでは、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間のメンバーから提供される InfoPath 2003 互換オブジェクト モデルを使用するマネージ コード フォーム テンプレートを作成する作業の始め方に関する情報を記載しています。
ms.openlocfilehash: 54d60e6d73ee224845c87c08f4de1e554e6182da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408055"
---
# <a name="get-started-developing-form-templates-using-the-infopath-object-model"></a><span data-ttu-id="eb9d4-104">InfoPath オブジェクトモデルを使用してフォームテンプレートの開発を開始する</span><span class="sxs-lookup"><span data-stu-id="eb9d4-104">Get started developing form templates using the InfoPath object model</span></span>

<span data-ttu-id="eb9d4-105">ここでは、[Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間のメンバーから提供される InfoPath 2003 互換オブジェクト モデルを使用するマネージ コード フォーム テンプレートを作成する作業の始め方に関する情報を記載しています。</span><span class="sxs-lookup"><span data-stu-id="eb9d4-105">This section provides information on how to get started creating managed-code form templates that work with the InfoPath 2003-compatible object model provided by members of the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="eb9d4-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="eb9d4-106">In this section</span></span>

- <span data-ttu-id="eb9d4-107">[infopath 2003 オブジェクトモデルを使用してフォームテンプレートを作成する](how-to-create-a-form-template-using-the-infopath-2003-object-model.md): infopath 2003 互換オブジェクトモデルで動作するビジネスロジックを含むフォームテンプレートを作成するための情報と手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="eb9d4-107">[Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md): Provides information and steps for creating form templates that contain business logic that works with the InfoPath 2003-compatible object model.</span></span>
    
- <span data-ttu-id="eb9d4-108">[[ウォークスルー] infopath 2003 オブジェクトモデルを使用して基本的なフォームテンプレートを作成およびデバッグ](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)する: infopath 2003 互換の infopath フォームテンプレートを作成および展開する方法の概要を説明するステップバイステップガイドです。オブジェクトモデル。</span><span class="sxs-lookup"><span data-stu-id="eb9d4-108">[Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md): A step-by-step guide that provides an introduction to creating and deploying a basic InfoPath form template that works with the InfoPath 2003-compatible object model.</span></span>
    
- <span data-ttu-id="eb9d4-109">[infopath 2003 オブジェクトモデルを使用してフォームテンプレートを開発するための一般的なタスク](common-tasks-for-developing-form-templates-using-infopath-object-model.md): infopath 2003 互換オブジェクトモデルに対して動作するビジネスロジックを使用したフォームテンプレートの開発に関してよく寄せられる質問に対する回答をすばやく見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="eb9d4-109">[Common Tasks for Developing Form Templates Using the InfoPath 2003 Object Model](common-tasks-for-developing-form-templates-using-infopath-object-model.md): Helps you quickly find the answers to common questions about developing form templates with business logic that works against the InfoPath 2003-compatible object model.</span></span>
    
- <span data-ttu-id="eb9d4-110">[infopath 2003 との互換性がない SemiTrust のメンバーを使用](how-to-use-microsoft-office-interop-infopath-semitrust-members.md)します。 [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)名前空間に追加された新しいオブジェクトモデルのメンバーを操作する方法について説明します。Office infopath 2007 および infopath 2010。</span><span class="sxs-lookup"><span data-stu-id="eb9d4-110">[Use Microsoft.Office.Interop.InfoPath.SemiTrust Members That Are Not Compatible with InfoPath 2003](how-to-use-microsoft-office-interop-infopath-semitrust-members.md): Discusses how to work with new object model members that were added to the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace in Office InfoPath 2007 and InfoPath 2010.</span></span> 
    
## <a name="related-sections"></a><span data-ttu-id="eb9d4-111">関連情報</span><span class="sxs-lookup"><span data-stu-id="eb9d4-111">Related sections</span></span>

- <span data-ttu-id="eb9d4-112">[infopath 2003 オブジェクトモデルを使用したフォームテンプレートの作成](creating-form-templates-using-the-infopath-2003-object-model.md): 初期化とクリーンアップのコード、イベントハンドラーを追加する方法、infopath の2003互換オブジェクトモデルを使用する infopath フォームテンプレートをデバッグおよび展開する方法、スレッドのサポートを行う方法について説明します。そして、Microsoft XML Core Services (MSXML) を使用します。</span><span class="sxs-lookup"><span data-stu-id="eb9d4-112">[Creating Form Templates Using the InfoPath 2003 Object Model](creating-form-templates-using-the-infopath-2003-object-model.md): Discusses initialization and clean-up code, how to add event handlers, how to debug and deploy InfoPath form templates that use the InfoPath 2003-compatible object model, threading support, and working with Microsoft XML Core Services (MSXML).</span></span>
    
- <span data-ttu-id="eb9d4-113">[infopath 2003 オブジェクトモデルに](understanding-the-infopath-2003-object-model.md)ついて: infopath 2003 互換オブジェクトモデルについて説明し、一般的なプログラミングタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="eb9d4-113">[Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md): Discusses the InfoPath 2003-compatible object model, and describes common programming tasks.</span></span>
    
- <span data-ttu-id="eb9d4-114">[infopath 2003 オブジェクトモデルを使用するフォームテンプレートのトラブルシューティング](troubleshoot-form-templates-that-use-infopath-object-model.md): infopath 2003 互換オブジェクトモデルで動作するフォームテンプレートを開発するときに発生する可能性のある一般的な問題を解決するためのヒントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="eb9d4-114">[Troubleshooting Form Templates That Use the InfoPath 2003 Object Model](troubleshoot-form-templates-that-use-infopath-object-model.md): Contains tips for solving common problems that you might encounter when developing form templates that work with the InfoPath 2003-compatible object model.</span></span>
    

