---
title: InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, creating,object models [InfoPath 2003], creating managed code form templates for InfoPath 2007,form templates [InfoPath 2007], creating InfoPath 2003-compatible
localization_priority: Normal
ms.assetid: e0513178-ddcb-4086-ab19-1bc80cf114cc
description: ここでは、初期化コードと後処理コード、イベント ハンドラーを追加する方法、InfoPath 2003 互換オブジェクト モデルを使用した InfoPath フォーム テンプレートのデバッグと展開の方法、スレッド サポート、および InfoPath マネージ コード ソリューションからの Microsoft XML Core Services (MSXML) の操作について説明します。
ms.openlocfilehash: 5069636dde87eb473a2b8bef4b58a6006d557085
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303746"
---
# <a name="creating-form-templates-using-the-infopath-2003-object-model"></a><span data-ttu-id="298f6-104">InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="298f6-104">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="298f6-105">ここでは、初期化コードと後処理コード、イベント ハンドラーを追加する方法、InfoPath 2003 互換オブジェクト モデルを使用した InfoPath フォーム テンプレートのデバッグと展開の方法、スレッド サポート、および InfoPath マネージ コード ソリューションからの Microsoft XML Core Services (MSXML) の操作について説明します。</span><span class="sxs-lookup"><span data-stu-id="298f6-105">This section discusses initialization and clean-up code, how to add event handlers, how to debug and deploy InfoPath form templates that use the InfoPath 2003-compatible object model, threading support, and working with Microsoft XML Core Services (MSXML) from InfoPath managed-code solutions.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="298f6-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="298f6-106">In this section</span></span>

[<span data-ttu-id="298f6-107">InfoPath 2003 オブジェクト モデルを使用する初期化コードと後処理コード</span><span class="sxs-lookup"><span data-stu-id="298f6-107">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
  
> <span data-ttu-id="298f6-108">プロジェクトの _Startup メソッドと _Shutdown メソッド内に初期化およびクリーンアップ コードを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="298f6-108">Discusses how to write initialization and clean-up code in the _Startup and _Shutdown methods of your project.</span></span>
    
[<span data-ttu-id="298f6-109">InfoPath 2003 オブジェクト モデルを使用してイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="298f6-109">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="298f6-110">イベント ハンドラーと、それぞれのイベント ハンドラーを識別するために適用する属性を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="298f6-110">Discusses how to add event handlers and the attributes that are applied to identify event handlers.</span></span>
    
[<span data-ttu-id="298f6-111">InfoPath 2003 オブジェクト モデルを使用して InfoPath プロジェクトをデバッグする</span><span class="sxs-lookup"><span data-stu-id="298f6-111">Debug InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="298f6-112">InfoPath マネージ コード プロジェクトをデバッグする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="298f6-112">Discusses how to debug InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="298f6-113">コードを含む InfoPath フォーム テンプレートを展開する</span><span class="sxs-lookup"><span data-stu-id="298f6-113">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)
  
> <span data-ttu-id="298f6-114">InfoPath マネージ コード プロジェクトを展開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="298f6-114">Discusses how to deploy InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="298f6-115">InfoPath 2003 オブジェクト モデルを使用する InfoPath プロジェクトにおけるスレッドのサポート</span><span class="sxs-lookup"><span data-stu-id="298f6-115">Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="298f6-116">InfoPath マネージ コード プロジェクトでのスレッド サポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="298f6-116">Discusses threading support in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="298f6-117">InfoPath 2003 オブジェクト モデルを使用して MSXML および System.Xml を操作する</span><span class="sxs-lookup"><span data-stu-id="298f6-117">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="298f6-118">InfoPath マネージ コード プロジェクト内で MSXML および System.Xml コードを使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="298f6-118">Discusses how to work with MSXML and System.Xml code in InfoPath managed-code projects.</span></span>
    

