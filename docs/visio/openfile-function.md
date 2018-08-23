---
title: OPENFILE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: ドキュメント ウィンドウがアクティブになりますが既に開いていない場合は、Microsoft Visio の図面を開きます。
ms.openlocfilehash: 7d4778fc4641465e88303b8515365172fd8be0ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805942"
---
# <a name="openfile-function"></a><span data-ttu-id="dbc68-103">OPENFILE 関数</span><span class="sxs-lookup"><span data-stu-id="dbc68-103">OPENFILE Function</span></span>

<span data-ttu-id="dbc68-104">ドキュメント ウィンドウがアクティブになりますが既に開いていない場合は、Microsoft Visio の図面を開きます。</span><span class="sxs-lookup"><span data-stu-id="dbc68-104">Opens a Microsoft Visio document, if it's not already open, and activates the document window.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dbc68-105">構文</span><span class="sxs-lookup"><span data-stu-id="dbc68-105">Syntax</span></span>

 <span data-ttu-id="dbc68-106">**OPENFILE**(_ファイル名_)</span><span class="sxs-lookup"><span data-stu-id="dbc68-106">**OPENFILE**( _"filename"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="dbc68-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dbc68-107">Parameters</span></span>

|<span data-ttu-id="dbc68-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="dbc68-108">**Name**</span></span>|<span data-ttu-id="dbc68-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="dbc68-109">**Required/Optional**</span></span>|<span data-ttu-id="dbc68-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="dbc68-110">**Data Type**</span></span>|<span data-ttu-id="dbc68-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="dbc68-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dbc68-112">filename</span><span class="sxs-lookup"><span data-stu-id="dbc68-112">_filename_</span></span> <br/> |<span data-ttu-id="dbc68-113">必須</span><span class="sxs-lookup"><span data-stu-id="dbc68-113">Required</span></span>  <br/> |<span data-ttu-id="dbc68-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="dbc68-114">**String**</span></span> <br/> |<span data-ttu-id="dbc68-115">開くには必要なファイルのパスを含むファイルの名前です。</span><span class="sxs-lookup"><span data-stu-id="dbc68-115">The name of the file, including file path, you want to open.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbc68-116">注釈</span><span class="sxs-lookup"><span data-stu-id="dbc68-116">Remarks</span></span>

<span data-ttu-id="dbc68-p101">複数の OPENFILE 関数を呼び出すと待ち行列に入り、評価する順序に従って実行されます。視覚的な編集ができるように、現在の Visio 図面をアクティブにすると (埋め込み先編集モード)、新しい Visio インスタンスが要求されたファイル名で起動されます。</span><span class="sxs-lookup"><span data-stu-id="dbc68-p101">Multiple OPENFILE function calls are queued and executed in order of evaluation. If the current Visio document is activated for visual (in-place) editing, a new Visio instance is launched with the requested file name.</span></span> 
  
<span data-ttu-id="dbc68-119">この関数は常に FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="dbc68-119">This function always returns FALSE.</span></span> 
  
<span data-ttu-id="dbc68-p102">以前のバージョンの Visio アプリケーションでは、この関数は _OPENFILE に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。</span><span class="sxs-lookup"><span data-stu-id="dbc68-p102">In earlier versions of the Visio application, this function appears as _OPENFILE. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="dbc68-122">例</span><span class="sxs-lookup"><span data-stu-id="dbc68-122">Example</span></span>

 `OPENFILE("C:/MyFile.vsdx")`
  
<span data-ttu-id="dbc68-123">新しいウィンドウで、指定されたファイル"MyFile.vsdx"を開くか、ファイルが既に開いている場合にウィンドウを表示します。</span><span class="sxs-lookup"><span data-stu-id="dbc68-123">Opens the specified file "MyFile.vsdx" in a new window, or activates the window if the file is already open.</span></span> 
  

