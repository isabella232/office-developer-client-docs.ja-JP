---
title: InfoPath 2003 オブジェクト モデルを理解する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, object model,InfoPath 2003-compatible object model,object models [InfoPath 2003]
localization_priority: Normal
ms.assetid: cd0a890b-5a8b-42c0-abdd-5ce28aff1ba1
description: ここでは、InfoPath マネージ コード ソリューションのオブジェクト モデルと一般的なプログラミング作業について説明します。
ms.openlocfilehash: 6fe649d068fd21b46e2a4d2824c1afbf8d9474ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799226"
---
# <a name="understanding-the-infopath-2003-object-model"></a><span data-ttu-id="5021b-104">InfoPath 2003 オブジェクト モデルを理解する</span><span class="sxs-lookup"><span data-stu-id="5021b-104">Understanding the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="5021b-105">ここでは、InfoPath マネージ コード ソリューションのオブジェクト モデルと一般的なプログラミング作業について説明します。</span><span class="sxs-lookup"><span data-stu-id="5021b-105">This section discusses the object model for InfoPath managed-code solutions, and describes common programming tasks.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="5021b-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="5021b-106">In this section</span></span>

[<span data-ttu-id="5021b-107">InfoPath 2003 互換オブジェクト モデル</span><span class="sxs-lookup"><span data-stu-id="5021b-107">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
  
> <span data-ttu-id="5021b-108">InfoPath マネージ コード プロジェクトで使用されるオブジェクト モデルの概要を紹介します。</span><span class="sxs-lookup"><span data-stu-id="5021b-108">Provides an overview of the object models used in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="5021b-109">InfoPath 2003 オブジェクト モデルを使用してアプリケーション データにアクセス</span><span class="sxs-lookup"><span data-stu-id="5021b-109">Access Application Data Using the InfoPath 2003 Object Model</span></span>](how-to-access-application-data-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="5021b-110">InfoPath アプリケーション、フォームの基になる XML ドキュメント、およびフォーム定義 (.xsf) ファイルに関する情報にアクセスする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5021b-110">Discusses how to access information about the InfoPath application, the form's underlying XML document, and the form definition (.xsf) file.</span></span>
    
[<span data-ttu-id="5021b-111">InfoPath 2003 オブジェクト モデルを使用して外部データ ソースのアクセス</span><span class="sxs-lookup"><span data-stu-id="5021b-111">Access External Data Sources Using the InfoPath 2003 Object Model</span></span>](how-to-access-external-data-sources-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="5021b-112">外部データ ソースのデータにアクセスする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5021b-112">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="5021b-113">InfoPath 2003 オブジェクト モデルを使用してフォーム データにアクセス</span><span class="sxs-lookup"><span data-stu-id="5021b-113">Access Form Data Using the InfoPath 2003 Object Model</span></span>](how-to-access-form-data-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="5021b-114">フォームの基になる XML ドキュメントに関する情報やそこに含まれるデータにアクセスする方法と、XML ドキュメントに対して何らかの操作を実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5021b-114">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="5021b-115">通知と、InfoPath 2003 オブジェクト モデルを使用してダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="5021b-115">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>](how-to-display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="5021b-116">InfoPath マネージ コード プロジェクトで警告とダイアログ ボックスを表示する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5021b-116">Discusses how to display alerts and dialog boxes in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="5021b-117">InfoPath 2003 オブジェクト モデルを使用してエラーを処理します。</span><span class="sxs-lookup"><span data-stu-id="5021b-117">Handle Errors Using the InfoPath 2003 Object Model</span></span>](how-to-handle-errors-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="5021b-118">InfoPath マネージ コード プロジェクトでエラーを処理する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5021b-118">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="5021b-119">フォーム、InfoPath 2003 オブジェクト モデルを使用してイベントに応答します。</span><span class="sxs-lookup"><span data-stu-id="5021b-119">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="5021b-120">ユーザーがフォームに入力する際に発生するイベントに応答するイベント ハンドラーを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5021b-120">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="5021b-121">InfoPath 2003 オブジェクト モデルを使用してフォーム ウィンドウを操作します。</span><span class="sxs-lookup"><span data-stu-id="5021b-121">Work with Form Windows Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-form-windows-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="5021b-122">フォーム ウィンドウを操作する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5021b-122">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="5021b-123">InfoPath 2003 オブジェクト モデルを使用してビューに関する作業します。</span><span class="sxs-lookup"><span data-stu-id="5021b-123">Work with Views Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-views-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="5021b-124">ビューを操作する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5021b-124">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="5021b-125">InfoPath 2003 オブジェクト モデルを使用して、デジタル署名を使用します。</span><span class="sxs-lookup"><span data-stu-id="5021b-125">Work with Digital Signatures Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-digital-signatures-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="5021b-126">デジタル署名を操作する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5021b-126">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="5021b-127">InfoPath 2003 オブジェクト モデルを使用してソリューションをオフラインで作業します。</span><span class="sxs-lookup"><span data-stu-id="5021b-127">Work with Offline Solutions Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-offline-solutions-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="5021b-128">オフライン ソリューションを操作する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5021b-128">Discusses how to work with offline solutions.</span></span>
    

