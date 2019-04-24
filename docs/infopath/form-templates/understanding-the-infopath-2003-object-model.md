---
title: InfoPath 2003 オブジェクト モデルについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, object model,InfoPath 2003-compatible object model,object models [InfoPath 2003]
localization_priority: Normal
ms.assetid: cd0a890b-5a8b-42c0-abdd-5ce28aff1ba1
description: ここでは、InfoPath マネージ コード ソリューションのオブジェクト モデルと一般的なプログラミング作業について説明します。
ms.openlocfilehash: 0c07201475bb7bfe24182faf61cc1bf6df733709
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299784"
---
# <a name="understanding-the-infopath-2003-object-model"></a><span data-ttu-id="2520b-104">InfoPath 2003 オブジェクト モデルを理解する</span><span class="sxs-lookup"><span data-stu-id="2520b-104">Understanding the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="2520b-105">ここでは、InfoPath マネージ コード ソリューションのオブジェクト モデルと一般的なプログラミング作業について説明します。</span><span class="sxs-lookup"><span data-stu-id="2520b-105">This section discusses the object model for InfoPath managed-code solutions, and describes common programming tasks.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="2520b-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="2520b-106">In this section</span></span>

[<span data-ttu-id="2520b-107">InfoPath 2003 互換オブジェクト モデル</span><span class="sxs-lookup"><span data-stu-id="2520b-107">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
  
> <span data-ttu-id="2520b-108">InfoPath マネージ コード プロジェクトで使用するオブジェクト モデルの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="2520b-108">Provides an overview of the object models used in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="2520b-109">InfoPath 2003 オブジェクト モデルを使用してアプリケーション データにアクセスする</span><span class="sxs-lookup"><span data-stu-id="2520b-109">Access Application Data Using the InfoPath 2003 Object Model</span></span>](how-to-access-application-data-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="2520b-110">InfoPath アプリケーション、フォームの基礎となる XML ドキュメント、およびフォーム定義 (.xsf) ファイルに関する情報にアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2520b-110">Discusses how to access information about the InfoPath application, the form's underlying XML document, and the form definition (.xsf) file.</span></span>
    
[<span data-ttu-id="2520b-111">InfoPath 2003 オブジェクト モデルを使用して外部データ ソースにアクセスする</span><span class="sxs-lookup"><span data-stu-id="2520b-111">Access External Data Sources Using the InfoPath 2003 Object Model</span></span>](how-to-access-external-data-sources-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="2520b-112">外部データ ソースからデータにアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2520b-112">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="2520b-113">InfoPath 2003 オブジェクト モデルを使用してフォーム データにアクセスする</span><span class="sxs-lookup"><span data-stu-id="2520b-113">Access Form Data Using the InfoPath 2003 Object Model</span></span>](how-to-access-form-data-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="2520b-114">フォームの基になる XML ドキュメントに関する情報やそこに含まれるデータにアクセスする方法と、XML ドキュメントに対して何らかの操作を実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="2520b-114">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="2520b-115">InfoPath 2003 オブジェクト モデルを使用して警告とダイアログ ボックスを表示する</span><span class="sxs-lookup"><span data-stu-id="2520b-115">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>](how-to-display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="2520b-116">InfoPath マネージ コード プロジェクトの通知やダイアログ ボックスを表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2520b-116">Discusses how to display alerts and dialog boxes in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="2520b-117">InfoPath 2003 オブジェクト モデルを使用してエラーを処理する</span><span class="sxs-lookup"><span data-stu-id="2520b-117">Handle Errors Using the InfoPath 2003 Object Model</span></span>](how-to-handle-errors-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="2520b-118">InfoPath マネージ コード プロジェクトのエラーを処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2520b-118">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="2520b-119">InfoPath 2003 オブジェクト モデルを使用してフォーム イベントに応答する</span><span class="sxs-lookup"><span data-stu-id="2520b-119">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="2520b-120">ユーザーがフォームに入力すると発生するイベントに応答するイベント ハンドラーの作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2520b-120">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="2520b-121">InfoPath 2003 オブジェクト モデルを使用してフォーム ウィンドウを操作する</span><span class="sxs-lookup"><span data-stu-id="2520b-121">Work with Form Windows Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-form-windows-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="2520b-122">フォーム ウィンドウを操作する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2520b-122">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="2520b-123">InfoPath 2003 オブジェクト モデルを使用してビューを操作する</span><span class="sxs-lookup"><span data-stu-id="2520b-123">Work with Views Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-views-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="2520b-124">ビューを操作する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2520b-124">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="2520b-125">InfoPath 2003 オブジェクト モデルを使用してデジタル署名を操作する</span><span class="sxs-lookup"><span data-stu-id="2520b-125">Work with Digital Signatures Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-digital-signatures-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="2520b-126">デジタル署名を操作する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2520b-126">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="2520b-127">InfoPath 2003 オブジェクト モデルを使用してオフライン ソリューションを操作する</span><span class="sxs-lookup"><span data-stu-id="2520b-127">Work with Offline Solutions Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-offline-solutions-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="2520b-128">オフライン ソリューションを操作する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2520b-128">Discusses how to work with offline solutions.</span></span>
    

