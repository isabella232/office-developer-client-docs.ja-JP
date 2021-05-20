---
title: '[ShdwOffsetX] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: 図形の影を図形から水平方向にオフセットする場合の距離を、ページの単位で指定します。
ms.openlocfilehash: fbc7d37fc8ba45f3219af6a4350301102954f23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431653"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a><span data-ttu-id="5f686-103">[ShdwOffsetX] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="5f686-103">ShdwOffsetX Cell (Page Properties Section)</span></span>

<span data-ttu-id="5f686-104">図形の影を図形から水平方向にオフセットする場合の距離を、ページの単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="5f686-104">Determines the distance in page units that a shape's drop shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f686-105">注釈</span><span class="sxs-lookup"><span data-stu-id="5f686-105">Remarks</span></span>

<span data-ttu-id="5f686-p101">この値は、[**ページ設定**] ダイアログ ボックスで設定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] 矢印をクリックします)。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、影のオフセットは変わりません。</span><span class="sxs-lookup"><span data-stu-id="5f686-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="5f686-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwOffsetX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5f686-109">To get a reference to the ShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5f686-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="5f686-110">Cell name:</span></span>  <br/> | <span data-ttu-id="5f686-111">ShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="5f686-111">ShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="5f686-112">プログラムから、インデックスによって [ShdwOffsetX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f686-112">To get a reference to the ShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5f686-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5f686-113">Section index:</span></span>  <br/> |<span data-ttu-id="5f686-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5f686-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5f686-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5f686-115">Row index:</span></span>  <br/> |<span data-ttu-id="5f686-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="5f686-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="5f686-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5f686-117">Cell index:</span></span>  <br/> |<span data-ttu-id="5f686-118">**visPageShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="5f686-118">**visPageShdwOffsetX**</span></span> <br/> |
   

