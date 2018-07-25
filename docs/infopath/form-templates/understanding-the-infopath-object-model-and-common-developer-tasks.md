---
title: InfoPath オブジェクト モデルと一般的な開発タスクについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- examples [infopath 2007],InfoPath 2007, developer tasks,developer tasks [InfoPath 2007],InfoPath 2007, object models,object models [InfoPath 2007]
localization_priority: Normal
ms.assetid: a2c18b72-426b-4f63-8454-187e96d26199
description: ここでは、InfoPath マネージ コード フォーム テンプレートの開発時に行う一般的な開発タスクに関する情報を記載しています。
ms.openlocfilehash: 9f0bbf36b2533b12ca3f31100c3abc21173d7c6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799217"
---
# <a name="understanding-the-infopath-object-model-and-common-developer-tasks"></a><span data-ttu-id="cff91-104">InfoPath オブジェクト モデルと一般的な開発タスクについて</span><span class="sxs-lookup"><span data-stu-id="cff91-104">Understanding the InfoPath Object Model and Common Developer Tasks</span></span>

<span data-ttu-id="cff91-105">ここでは、InfoPath マネージ コード フォーム テンプレートの開発時に行う一般的な開発タスクに関する情報を記載しています。</span><span class="sxs-lookup"><span data-stu-id="cff91-105">This section provides information on common developer tasks when developing InfoPath managed code form templates.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="cff91-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="cff91-106">In this section</span></span>

[<span data-ttu-id="cff91-107">アプリケーション データにアクセスする</span><span class="sxs-lookup"><span data-stu-id="cff91-107">Access Application Data?</span></span>](how-to-access-application-data.md)
  
> <span data-ttu-id="cff91-108">InfoPath アプリケーションに関する情報にアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cff91-108">Discusses how to access information about the InfoPath application.</span></span>
    
[<span data-ttu-id="cff91-109">フォーム イベントに応答する</span><span class="sxs-lookup"><span data-stu-id="cff91-109">Respond to Form Events?</span></span>](how-to-respond-to-form-events.md)
  
> <span data-ttu-id="cff91-110">ユーザーがフォームに入力すると発生するイベントに応答するイベント ハンドラーの作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cff91-110">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="cff91-111">フォーム データにアクセスする</span><span class="sxs-lookup"><span data-stu-id="cff91-111">Access Form Data?</span></span>](how-to-access-form-data.md)
  
> <span data-ttu-id="cff91-112">フォームの基になる XML ドキュメントに関する情報やそこに含まれるデータにアクセスする方法と、XML ドキュメントに対して何らかの操作を実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="cff91-112">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="cff91-113">外部データ ソースにアクセスする</span><span class="sxs-lookup"><span data-stu-id="cff91-113">Access External Data Sources?</span></span>](how-to-access-external-data-sources.md)
  
> <span data-ttu-id="cff91-114">外部データ ソースからデータにアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cff91-114">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="cff91-115">実行時環境を決定する条件付きロジックを書く</span><span class="sxs-lookup"><span data-stu-id="cff91-115">How to: Write Conditional Logic That Determines the Run-time Environment</span></span>](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
> <span data-ttu-id="cff91-116">InfoPath、Web ブラウザー、またはモバイル ブラウザーでフォームが開かれたかによって、異なる操作を行うコードを書く方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="cff91-116">Discusses how to write code that performs a different action depending on whether the form is open in InfoPath, a Web browser, or a mobile browser.</span></span>
    
[<span data-ttu-id="cff91-117">フォーム ウィンドウを操作する</span><span class="sxs-lookup"><span data-stu-id="cff91-117">Work with Form Windows?</span></span>](how-to-work-with-form-windows.md)
  
> <span data-ttu-id="cff91-118">フォーム ウィンドウを操作する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cff91-118">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="cff91-119">ビューを操作する</span><span class="sxs-lookup"><span data-stu-id="cff91-119">Work with Views?</span></span>](how-to-work-with-views.md)
  
> <span data-ttu-id="cff91-120">ビューを操作する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cff91-120">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="cff91-121">オフライン ソリューションを操作する</span><span class="sxs-lookup"><span data-stu-id="cff91-121">Work with Offline Solutions?</span></span>](how-to-work-with-offline-solutions.md)
  
> <span data-ttu-id="cff91-122">オフライン ソリューションを操作する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cff91-122">Discusses how to work with offline solutions.</span></span>
    
[<span data-ttu-id="cff91-123">デジタル署名を操作する</span><span class="sxs-lookup"><span data-stu-id="cff91-123">Work with Digital Signatures?</span></span>](how-to-work-with-digital-signatures.md)
  
> <span data-ttu-id="cff91-124">デジタル署名を操作する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cff91-124">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="cff91-125">エラーを処理する</span><span class="sxs-lookup"><span data-stu-id="cff91-125">Handle errors.</span></span>](how-to-handle-errors.md)
  
> <span data-ttu-id="cff91-126">InfoPath マネージ コード プロジェクトのエラーを処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cff91-126">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="cff91-127">Information Rights Management の設定を操作する</span><span class="sxs-lookup"><span data-stu-id="cff91-127">Work with Information Rights Management Settings?</span></span>](how-to-work-with-information-rights-management-settings.md)
  
> <span data-ttu-id="cff91-128">Information Rights Management (IRM) の設定を操作する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cff91-128">Discusses how to work with Information Rights Management (IRM) settings.</span></span>
    
[<span data-ttu-id="cff91-129">カスタム アセンブリを追加および参照する</span><span class="sxs-lookup"><span data-stu-id="cff91-129">How to: Add and Reference Custom Assemblies</span></span>](how-to-add-and-reference-custom-assemblies.md)
  
> <span data-ttu-id="cff91-130">フォーム テンプレート プロジェクトにカスタム アセンブリを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cff91-130">Discusses how to add custom assemblies to a form template project.</span></span>
    

