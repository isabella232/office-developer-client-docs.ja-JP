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
ms.openlocfilehash: 16d49b24b2eed3b7fe15621d47663a94f1958cfa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799101"
---
# <a name="creating-form-templates-using-the-infopath-2003-object-model"></a><span data-ttu-id="1e2a3-104">InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="1e2a3-104">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="1e2a3-105">ここでは、初期化コードと後処理コード、イベント ハンドラーを追加する方法、InfoPath 2003 互換オブジェクト モデルを使用した InfoPath フォーム テンプレートのデバッグと展開の方法、スレッド サポート、および InfoPath マネージ コード ソリューションからの Microsoft XML Core Services (MSXML) の操作について説明します。</span><span class="sxs-lookup"><span data-stu-id="1e2a3-105">This section discusses initialization and clean-up code, how to add event handlers, how to debug and deploy InfoPath form templates that use the InfoPath 2003-compatible object model, threading support, and working with Microsoft XML Core Services (MSXML) from InfoPath managed-code solutions.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="1e2a3-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="1e2a3-106">In this section</span></span>

[<span data-ttu-id="1e2a3-107">InfoPath 2003 オブジェクト モデルを使用する初期化コードと後処理コード</span><span class="sxs-lookup"><span data-stu-id="1e2a3-107">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
  
> <span data-ttu-id="1e2a3-108">プロジェクトの _Startup メソッドに初期化コードを記述し、_Shutdown メソッドに後処理コードを記述する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="1e2a3-108">Discusses how to write initialization and clean-up code in the _Startup and _Shutdown methods of your project.</span></span>
    
[<span data-ttu-id="1e2a3-109">InfoPath 2003 オブジェクト モデルを使用してイベント ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="1e2a3-109">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="1e2a3-110">イベント ハンドラーと、イベント ハンドラーを識別するために適用される属性を追加する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="1e2a3-110">Discusses how to add event handlers and the attributes that are applied to identify event handlers.</span></span>
    
[<span data-ttu-id="1e2a3-111">InfoPath 2003 オブジェクト モデルを使用して InfoPath プロジェクトをデバッグします。</span><span class="sxs-lookup"><span data-stu-id="1e2a3-111">Debug InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="1e2a3-112">InfoPath マネージ コード プロジェクトをデバッグする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="1e2a3-112">Discusses how to debug InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="1e2a3-113">コードを含む InfoPath フォーム テンプレートを展開します。</span><span class="sxs-lookup"><span data-stu-id="1e2a3-113">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)
  
> <span data-ttu-id="1e2a3-114">InfoPath マネージ コード プロジェクトを展開する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="1e2a3-114">Discusses how to deploy InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="1e2a3-115">InfoPath 2003 オブジェクト モデルを使用する InfoPath プロジェクトにおけるスレッドのサポート</span><span class="sxs-lookup"><span data-stu-id="1e2a3-115">Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="1e2a3-116">InfoPath マネージ コード プロジェクトでのスレッド サポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1e2a3-116">Discusses threading support in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="1e2a3-117">InfoPath 2003 オブジェクト モデルを使用して MSXML および System.Xml を操作する</span><span class="sxs-lookup"><span data-stu-id="1e2a3-117">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="1e2a3-118">InfoPath マネージ コード プロジェクト内で MSXML および System.Xml コードを使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="1e2a3-118">Discusses how to work with MSXML and System.Xml code in InfoPath managed-code projects.</span></span>
    
