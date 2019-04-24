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
description: pagename という名前のページが、現在アクティブなウィンドウに表示されます。
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302969"
---
# <a name="gotopage-function"></a><span data-ttu-id="caee9-103">GOTOPAGE 関数</span><span class="sxs-lookup"><span data-stu-id="caee9-103">GOTOPAGE Function</span></span>

<span data-ttu-id="caee9-104">*pagename*という名前のページが、現在アクティブなウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="caee9-104">Displays the page that has the name  *pagename*  in the currently active window.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="caee9-105">構文</span><span class="sxs-lookup"><span data-stu-id="caee9-105">Syntax</span></span>

<span data-ttu-id="caee9-106">GOTOPAGE ("\* \* *pagename* \* \*")</span><span class="sxs-lookup"><span data-stu-id="caee9-106">GOTOPAGE(" \*\* *pagename* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="caee9-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="caee9-107">Parameters</span></span>

|<span data-ttu-id="caee9-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="caee9-108">**Name**</span></span>|<span data-ttu-id="caee9-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="caee9-109">**Required/Optional**</span></span>|<span data-ttu-id="caee9-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="caee9-110">**Data Type**</span></span>|<span data-ttu-id="caee9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="caee9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="caee9-112">_pagename_</span><span class="sxs-lookup"><span data-stu-id="caee9-112">_pagename_</span></span> <br/> |<span data-ttu-id="caee9-113">必須</span><span class="sxs-lookup"><span data-stu-id="caee9-113">Required</span></span>  <br/> |<span data-ttu-id="caee9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="caee9-114">**String**</span></span> <br/> |<span data-ttu-id="caee9-115">移動先のページの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="caee9-115">The name of the page to go to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="caee9-116">解説</span><span class="sxs-lookup"><span data-stu-id="caee9-116">Remarks</span></span>

<span data-ttu-id="caee9-117">ウィンドウに既にそのページが表示されている場合、そのウィンドウがアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="caee9-117">If a window is already displaying the page, that window becomes active.</span></span> <span data-ttu-id="caee9-118">*pagename*が存在しない場合、アプリケーションは https:// *pagename* /に移動しようとします。</span><span class="sxs-lookup"><span data-stu-id="caee9-118">If  *pagename*  does not exist, the application attempts to navigate to https://  *pagename*  /.</span></span> <span data-ttu-id="caee9-119">Visio が埋め込み先サーバーとして機能している場合は、GOTOPAGE 関数は無効になります。</span><span class="sxs-lookup"><span data-stu-id="caee9-119">If Visio is acting as an in-place server, the GOTOPAGE function has no effect.</span></span> 
  
<span data-ttu-id="caee9-120">DOS、UNC、または URL のパスに従って移動するには、HYPERLINK 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="caee9-120">You can use the HYPERLINK function to navigate to any DOS, UNC, or URL path.</span></span> 
  
<span data-ttu-id="caee9-p102">以前のバージョンの Visio 製品では、この関数は _GOTOPAGE に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。</span><span class="sxs-lookup"><span data-stu-id="caee9-p102">In earlier versions of Visio products, this function appears as _GOTOPAGE. Visio versions 4.0 and later accept either style.</span></span> 
  

