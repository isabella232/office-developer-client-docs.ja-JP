---
title: InfoPath オブジェクト モデルを使用したフォーム テンプレートの開発を開始する
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
# <a name="get-started-developing-form-templates-using-the-infopath-object-model"></a><span data-ttu-id="643aa-104">InfoPath オブジェクト モデルを使用したフォーム テンプレートの開発を開始する</span><span class="sxs-lookup"><span data-stu-id="643aa-104">Get started developing form templates using the InfoPath object model</span></span>

<span data-ttu-id="643aa-105">ここでは、[Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間のメンバーから提供される InfoPath 2003 互換オブジェクト モデルを使用するマネージ コード フォーム テンプレートを作成する作業の始め方に関する情報を記載しています。</span><span class="sxs-lookup"><span data-stu-id="643aa-105">This section provides information on how to get started creating managed-code form templates that work with the InfoPath 2003-compatible object model provided by members of the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="643aa-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="643aa-106">In this section</span></span>

- <span data-ttu-id="643aa-107">[InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)オブジェクト モデルを使用してフォーム テンプレートを作成する : InfoPath 2003 互換オブジェクト モデルで動作するビジネス ロジックを含むフォーム テンプレートを作成するための情報と手順を示します。</span><span class="sxs-lookup"><span data-stu-id="643aa-107">[Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md): Provides information and steps for creating form templates that contain business logic that works with the InfoPath 2003-compatible object model.</span></span>
    
- <span data-ttu-id="643aa-108">[チュートリアル: InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)オブジェクト モデルを使用した基本フォーム テンプレートの作成とデバッグ: InfoPath 2003 互換オブジェクト モデルで動作する基本的な InfoPath フォーム テンプレートの作成と展開の概要を示すステップ バイ ステップ ガイド。</span><span class="sxs-lookup"><span data-stu-id="643aa-108">[Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md): A step-by-step guide that provides an introduction to creating and deploying a basic InfoPath form template that works with the InfoPath 2003-compatible object model.</span></span>
    
- <span data-ttu-id="643aa-109">[InfoPath 2003](common-tasks-for-developing-form-templates-using-infopath-object-model.md)オブジェクト モデルを使用してフォーム テンプレートを開発するための一般的なタスク: InfoPath 2003 互換オブジェクト モデルに対して動作するビジネス ロジックを使用してフォーム テンプレートを開発する方法に関する一般的な質問に対する回答をすばやく見つけるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="643aa-109">[Common Tasks for Developing Form Templates Using the InfoPath 2003 Object Model](common-tasks-for-developing-form-templates-using-infopath-object-model.md): Helps you quickly find the answers to common questions about developing form templates with business logic that works against the InfoPath 2003-compatible object model.</span></span>
    
- <span data-ttu-id="643aa-110">[Microsoft を使用します。Office.Interop.InfoPath.SemiTrust メンバー InfoPath 2003](how-to-use-microsoft-office-interop-infopath-semitrust-members.md)と互換性がない : Office InfoPath 2007 および InfoPath 2010 の[Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)名前空間に追加された新しいオブジェクト モデル メンバーを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="643aa-110">[Use Microsoft.Office.Interop.InfoPath.SemiTrust Members That Are Not Compatible with InfoPath 2003](how-to-use-microsoft-office-interop-infopath-semitrust-members.md): Discusses how to work with new object model members that were added to the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace in Office InfoPath 2007 and InfoPath 2010.</span></span> 
    
## <a name="related-sections"></a><span data-ttu-id="643aa-111">関連情報</span><span class="sxs-lookup"><span data-stu-id="643aa-111">Related sections</span></span>

- <span data-ttu-id="643aa-112">フォーム テンプレートの作成[InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)オブジェクト モデルを使用する : 初期化とクリーンアップ コード、イベント ハンドラーの追加方法、InfoPath 2003 互換オブジェクト モデルを使用する InfoPath フォーム テンプレートのデバッグと展開方法、スレッドのサポート、および Microsoft XML Core Services (MSXML) の操作について説明します。</span><span class="sxs-lookup"><span data-stu-id="643aa-112">[Creating Form Templates Using the InfoPath 2003 Object Model](creating-form-templates-using-the-infopath-2003-object-model.md): Discusses initialization and clean-up code, how to add event handlers, how to debug and deploy InfoPath form templates that use the InfoPath 2003-compatible object model, threading support, and working with Microsoft XML Core Services (MSXML).</span></span>
    
- <span data-ttu-id="643aa-113">[InfoPath 2003 オブジェクト](understanding-the-infopath-2003-object-model.md)モデルについて : InfoPath 2003 互換オブジェクト モデルについて説明し、一般的なプログラミング タスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="643aa-113">[Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md): Discusses the InfoPath 2003-compatible object model, and describes common programming tasks.</span></span>
    
- <span data-ttu-id="643aa-114">[InfoPath 2003](troubleshoot-form-templates-that-use-infopath-object-model.md)オブジェクト モデルを使用するフォーム テンプレートのトラブルシューティング : InfoPath 2003 互換オブジェクト モデルで動作するフォーム テンプレートを開発するときに発生する可能性のある一般的な問題を解決するためのヒントが含まれる。</span><span class="sxs-lookup"><span data-stu-id="643aa-114">[Troubleshooting Form Templates That Use the InfoPath 2003 Object Model](troubleshoot-form-templates-that-use-infopath-object-model.md): Contains tips for solving common problems that you might encounter when developing form templates that work with the InfoPath 2003-compatible object model.</span></span>
    

