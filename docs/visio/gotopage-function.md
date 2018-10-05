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
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397150"
---
# <a name="gotopage-function"></a><span data-ttu-id="a38c3-103">GOTOPAGE 関数</span><span class="sxs-lookup"><span data-stu-id="a38c3-103">GOTOPAGE Function</span></span>

<span data-ttu-id="a38c3-104">現在作業中のウィンドウで名前の*指定した pagename*を持つページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a38c3-104">Displays the page that has the name  *pagename*  in the currently active window.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a38c3-105">構文</span><span class="sxs-lookup"><span data-stu-id="a38c3-105">Syntax</span></span>

<span data-ttu-id="a38c3-106">GOTOPAGE ("\* \**指定した pagename* \* \*")</span><span class="sxs-lookup"><span data-stu-id="a38c3-106">GOTOPAGE(" \*\* *pagename* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a38c3-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a38c3-107">Parameters</span></span>

|<span data-ttu-id="a38c3-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="a38c3-108">**Name**</span></span>|<span data-ttu-id="a38c3-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="a38c3-109">**Required/Optional**</span></span>|<span data-ttu-id="a38c3-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="a38c3-110">**Data Type**</span></span>|<span data-ttu-id="a38c3-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="a38c3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a38c3-112">_pagename_</span><span class="sxs-lookup"><span data-stu-id="a38c3-112">_pagename_</span></span> <br/> |<span data-ttu-id="a38c3-113">必須</span><span class="sxs-lookup"><span data-stu-id="a38c3-113">Required</span></span>  <br/> |<span data-ttu-id="a38c3-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="a38c3-114">**String**</span></span> <br/> |<span data-ttu-id="a38c3-115">移動先のページの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a38c3-115">The name of the page to go to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a38c3-116">注釈</span><span class="sxs-lookup"><span data-stu-id="a38c3-116">Remarks</span></span>

<span data-ttu-id="a38c3-117">ウィンドウには、既にページが表示されて、そのウィンドウがアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="a38c3-117">If a window is already displaying the page, that window becomes active.</span></span> <span data-ttu-id="a38c3-118">アプリケーションが https://*指定した pagename*に移動しようとした*pagename*が存在しない場合とします。</span><span class="sxs-lookup"><span data-stu-id="a38c3-118">If  *pagename*  does not exist, the application attempts to navigate to https://  *pagename*  /.</span></span> <span data-ttu-id="a38c3-119">Visio が埋め込み先サーバーとして動作している場合は、GOTOPAGE 関数に影響はありません。</span><span class="sxs-lookup"><span data-stu-id="a38c3-119">If Visio is acting as an in-place server, the GOTOPAGE function has no effect.</span></span> 
  
<span data-ttu-id="a38c3-120">DOS、UNC、または URL のパスに従って移動するには、HYPERLINK 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="a38c3-120">You can use the HYPERLINK function to navigate to any DOS, UNC, or URL path.</span></span> 
  
<span data-ttu-id="a38c3-p102">以前のバージョンの Visio 製品では、この関数は _GOTOPAGE に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。</span><span class="sxs-lookup"><span data-stu-id="a38c3-p102">In earlier versions of Visio products, this function appears as _GOTOPAGE. Visio versions 4.0 and later accept either style.</span></span> 
  

