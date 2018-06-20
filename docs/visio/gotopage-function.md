---
title: GOTOPAGE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: 現在作業中のウィンドウで名前の指定した pagename を持つページが表示されます。
ms.openlocfilehash: 67f8a79b854fd6f2ae47e39877ffcdbe4a1be5cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805494"
---
# <a name="gotopage-function"></a><span data-ttu-id="31544-103">GOTOPAGE 関数</span><span class="sxs-lookup"><span data-stu-id="31544-103">GOTOPAGE Function</span></span>

<span data-ttu-id="31544-104">現在作業中のウィンドウで名前の*指定した pagename*を持つページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="31544-104">Displays the page that has the name  *pagename*  in the currently active window.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="31544-105">構文</span><span class="sxs-lookup"><span data-stu-id="31544-105">Syntax</span></span>

<span data-ttu-id="31544-106">GOTOPAGE ("* **指定した pagename* * *")</span><span class="sxs-lookup"><span data-stu-id="31544-106">GOTOPAGE(" ** *pagename* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="31544-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="31544-107">Parameters</span></span>

|<span data-ttu-id="31544-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="31544-108">**Name**</span></span>|<span data-ttu-id="31544-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="31544-109">**Required/Optional**</span></span>|<span data-ttu-id="31544-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="31544-110">**Data Type**</span></span>|<span data-ttu-id="31544-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="31544-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="31544-112">_pagename_</span><span class="sxs-lookup"><span data-stu-id="31544-112">_pagename_</span></span> <br/> |<span data-ttu-id="31544-113">必須</span><span class="sxs-lookup"><span data-stu-id="31544-113">Required</span></span>  <br/> |<span data-ttu-id="31544-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="31544-114">**String**</span></span> <br/> |<span data-ttu-id="31544-115">移動先のページの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="31544-115">The name of the page to go to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31544-116">注釈</span><span class="sxs-lookup"><span data-stu-id="31544-116">Remarks</span></span>

<span data-ttu-id="31544-117">ウィンドウには、既にページが表示されて、そのウィンドウがアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="31544-117">If a window is already displaying the page, that window becomes active.</span></span> <span data-ttu-id="31544-118">アプリケーションが http://*指定した pagename*に移動しようとした*pagename*が存在しない場合とします。</span><span class="sxs-lookup"><span data-stu-id="31544-118">If  *pagename*  does not exist, the application attempts to navigate to http://  *pagename*  /.</span></span> <span data-ttu-id="31544-119">Visio が埋め込み先サーバーとして動作している場合は、GOTOPAGE 関数に影響はありません。</span><span class="sxs-lookup"><span data-stu-id="31544-119">If Visio is acting as an in-place server, the GOTOPAGE function has no effect.</span></span> 
  
<span data-ttu-id="31544-120">DOS、UNC、または URL のパスに従って移動するには、HYPERLINK 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="31544-120">You can use the HYPERLINK function to navigate to any DOS, UNC, or URL path.</span></span> 
  
<span data-ttu-id="31544-p102">以前のバージョンの Visio 製品では、この関数は _GOTOPAGE に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。</span><span class="sxs-lookup"><span data-stu-id="31544-p102">In earlier versions of Visio products, this function appears as _GOTOPAGE. Visio versions 4.0 and later accept either style.</span></span> 
  

