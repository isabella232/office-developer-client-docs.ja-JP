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
description: まだ開いていない場合Visio Microsoft ドキュメントを開き、ドキュメント ウィンドウをアクティブにします。
ms.openlocfilehash: 5a89a658e560d144007ec19796de82b9949bea82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419577"
---
# <a name="openfile-function"></a><span data-ttu-id="da0c9-103">OPENFILE 関数</span><span class="sxs-lookup"><span data-stu-id="da0c9-103">OPENFILE Function</span></span>

<span data-ttu-id="da0c9-104">まだ開いていない場合Visio Microsoft ドキュメントを開き、ドキュメント ウィンドウをアクティブにします。</span><span class="sxs-lookup"><span data-stu-id="da0c9-104">Opens a Microsoft Visio document, if it's not already open, and activates the document window.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="da0c9-105">構文</span><span class="sxs-lookup"><span data-stu-id="da0c9-105">Syntax</span></span>

 <span data-ttu-id="da0c9-106">**OPENFILE**( _"filename" )_</span><span class="sxs-lookup"><span data-stu-id="da0c9-106">**OPENFILE**( _"filename"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="da0c9-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="da0c9-107">Parameters</span></span>

|<span data-ttu-id="da0c9-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="da0c9-108">**Name**</span></span>|<span data-ttu-id="da0c9-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="da0c9-109">**Required/Optional**</span></span>|<span data-ttu-id="da0c9-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="da0c9-110">**Data Type**</span></span>|<span data-ttu-id="da0c9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="da0c9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="da0c9-112">_filename_</span><span class="sxs-lookup"><span data-stu-id="da0c9-112">_filename_</span></span> <br/> |<span data-ttu-id="da0c9-113">必須</span><span class="sxs-lookup"><span data-stu-id="da0c9-113">Required</span></span>  <br/> |<span data-ttu-id="da0c9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="da0c9-114">**String**</span></span> <br/> |<span data-ttu-id="da0c9-115">開くファイル パスを含むファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="da0c9-115">The name of the file, including file path, you want to open.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da0c9-116">注釈</span><span class="sxs-lookup"><span data-stu-id="da0c9-116">Remarks</span></span>

<span data-ttu-id="da0c9-p101">複数の OPENFILE 関数を呼び出すと待ち行列に入り、評価する順序に従って実行されます。視覚的な編集ができるように、現在の Visio 図面をアクティブにすると (埋め込み先編集モード)、新しい Visio インスタンスが要求されたファイル名で起動されます。</span><span class="sxs-lookup"><span data-stu-id="da0c9-p101">Multiple OPENFILE function calls are queued and executed in order of evaluation. If the current Visio document is activated for visual (in-place) editing, a new Visio instance is launched with the requested file name.</span></span> 
  
<span data-ttu-id="da0c9-119">この関数は常に FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="da0c9-119">This function always returns FALSE.</span></span> 
  
<span data-ttu-id="da0c9-p102">以前のバージョンの Visio アプリケーションでは、この関数は _OPENFILE に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。</span><span class="sxs-lookup"><span data-stu-id="da0c9-p102">In earlier versions of the Visio application, this function appears as _OPENFILE. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="da0c9-122">例</span><span class="sxs-lookup"><span data-stu-id="da0c9-122">Example</span></span>

 `OPENFILE("C:/MyFile.vsdx")`
  
<span data-ttu-id="da0c9-123">指定したファイル "MyFile.vsdx" を新しいウィンドウで開くか、ファイルが既に開いている場合はウィンドウをアクティブにします。</span><span class="sxs-lookup"><span data-stu-id="da0c9-123">Opens the specified file "MyFile.vsdx" in a new window, or activates the window if the file is already open.</span></span> 
  

