---
title: RUNADDONWARGS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
localization_priority: Normal
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: 文字列を実行し、コマンドライン引数を文字列としてプログラムに渡します。
ms.openlocfilehash: 7bc05a0cbf32550d1e39bee39bec83101882cf19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806339"
---
# <a name="runaddonwargs-function"></a><span data-ttu-id="750d1-103">RUNADDONWARGS 関数</span><span class="sxs-lookup"><span data-stu-id="750d1-103">RUNADDONWARGS Function</span></span>

<span data-ttu-id="750d1-104">_文字列_を実行し、コマンド ・ ライン_引数_を文字列としてプログラムに渡します。</span><span class="sxs-lookup"><span data-stu-id="750d1-104">Runs  _string_ and passes the command line  _arguments_ to the program as a string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="750d1-105">構文</span><span class="sxs-lookup"><span data-stu-id="750d1-105">Syntax</span></span>

<span data-ttu-id="750d1-106">RUNADDONWARGS ("* **文字列** *","* **引数** *")</span><span class="sxs-lookup"><span data-stu-id="750d1-106">RUNADDONWARGS(" ** *string* ** "," ** *arguments* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="750d1-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="750d1-107">Parameters</span></span>

|<span data-ttu-id="750d1-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="750d1-108">**Name**</span></span>|<span data-ttu-id="750d1-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="750d1-109">**Required/Optional**</span></span>|<span data-ttu-id="750d1-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="750d1-110">**Data Type**</span></span>|<span data-ttu-id="750d1-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="750d1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="750d1-112">_string_</span><span class="sxs-lookup"><span data-stu-id="750d1-112">_string_</span></span> <br/> |<span data-ttu-id="750d1-113">必須</span><span class="sxs-lookup"><span data-stu-id="750d1-113">Required</span></span>  <br/> |<span data-ttu-id="750d1-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="750d1-114">**String**</span></span> <br/> | <span data-ttu-id="750d1-115">アドオンの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="750d1-115">The name of an add-on.</span></span>  <br/> |
| <span data-ttu-id="750d1-116">_arguments_</span><span class="sxs-lookup"><span data-stu-id="750d1-116">_arguments_</span></span> <br/> |<span data-ttu-id="750d1-117">必須</span><span class="sxs-lookup"><span data-stu-id="750d1-117">Required</span></span>  <br/> |<span data-ttu-id="750d1-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="750d1-118">**String**</span></span> <br/> |<span data-ttu-id="750d1-119">ユーザーのプログラムに渡す引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="750d1-119">Arguments to pass to your program.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="750d1-120">注釈</span><span class="sxs-lookup"><span data-stu-id="750d1-120">Remarks</span></span>

<span data-ttu-id="750d1-121">実際には、_引数_は 50 文字以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="750d1-121">In practice,  _arguments_ should be 50 or fewer characters.</span></span> <span data-ttu-id="750d1-122">RUNADDONWARGS 関数を使用すると、アクションまたはイベント セル、セルに、アドオンなどのプログラムをバインドします。</span><span class="sxs-lookup"><span data-stu-id="750d1-122">Use the RUNADDONWARGS function to bind a program, such as an add-on, to a cell, for example, to an Action or Events cell.</span></span> 
  
<span data-ttu-id="750d1-p102">RUNADDONWARGS 関数は、アプリケーションの **Addons** コレクションのメンバーであるアドオンのみ実行できます。このコレクションのメンバーになるためには、アドオンの EXE ファイルまたは VSL ファイルが次の条件を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="750d1-p102">The RUNADDONWARGS function can only run add-ons that are members of the application's **Addons** collection. To be present in that collection, an add-on must be an EXE file or VSL file that is:</span></span> 
  
- <span data-ttu-id="750d1-125">アプリケーションの**起動時**または**アドオン**のパスにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="750d1-125">Installed in the application's **Startup** or **Addons** path.</span></span> 
    
- <span data-ttu-id="750d1-126">**Addons** コレクションの **Add** メソッドを使用してプログラムから追加されている。</span><span class="sxs-lookup"><span data-stu-id="750d1-126">Added programmatically by using the **Add** method of the **Addons** collection.</span></span> 
    
<span data-ttu-id="750d1-127">Visio でのコードの実行に関する詳細については、この『シェイプシート リファレンス』の「[Visio のセキュリティ設定とコードの実行について](about-security-settings-and-running-code-in-visio-shapesheet.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="750d1-127">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="750d1-p103">以前のバージョンの Visio では、この関数は _RUNADDONWARGS に相当します。Visio アプリケーション バージョン 4.0 以降では、どちらのスタイルも使用できます。</span><span class="sxs-lookup"><span data-stu-id="750d1-p103">In earlier versions of Visio, this function appears as _RUNADDONWARGS. Visio application versions 4.0 and later accept either style.</span></span>
  
## <a name="example"></a><span data-ttu-id="750d1-130">例</span><span class="sxs-lookup"><span data-stu-id="750d1-130">Example</span></span>

<span data-ttu-id="750d1-131">RUNADDONWARGS ("GRAPHMKR。EXE"、"/GraphMaker = スタック」)</span><span class="sxs-lookup"><span data-stu-id="750d1-131">RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack")</span></span> 
  
<span data-ttu-id="750d1-132">アドオン Graphmkr.exe を起動し、これに引数 /GraphMaker=Stack を渡します。</span><span class="sxs-lookup"><span data-stu-id="750d1-132">Launches the add-on Graphmkr.exe and passes it the argument /GraphMaker=Stack.</span></span> 
  

