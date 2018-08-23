---
title: '[ShdwOffsetY] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: 図形の影を図形から垂直方向にオフセットする場合の距離を、ページの単位で指定します。
ms.openlocfilehash: 0228fef00230dd1517d20067fda855225cef5533
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806473"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="47712-103">[ShdwOffsetY] セル ([ページのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="47712-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="47712-104">図形の影を図形から垂直方向にオフセットする場合の距離を、ページの単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="47712-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47712-105">注釈</span><span class="sxs-lookup"><span data-stu-id="47712-105">Remarks</span></span>

<span data-ttu-id="47712-p101">この値は、[**ページ設定**] ダイアログ ボックスで設定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] 矢印をクリックします)。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、影のオフセットは変わりません。</span><span class="sxs-lookup"><span data-stu-id="47712-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="47712-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwOffsetY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="47712-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="47712-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="47712-110">Cell name:</span></span>  <br/> | <span data-ttu-id="47712-111">ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="47712-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="47712-112">プログラムから、インデックスによって [ShdwOffsetY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="47712-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="47712-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="47712-113">Section index:</span></span>  <br/> |<span data-ttu-id="47712-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="47712-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="47712-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="47712-115">Row index:</span></span>  <br/> |<span data-ttu-id="47712-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="47712-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="47712-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="47712-117">Cell index:</span></span>  <br/> |<span data-ttu-id="47712-118">**visPageShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="47712-118">**visPageShdwOffsetY**</span></span> <br/> |
   

