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
ms.openlocfilehash: 9aec108146e329d7a8161acc4ca7cdcb19424eff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806456"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a><span data-ttu-id="6a0df-103">[ShdwOffsetX] セル ([ページのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="6a0df-103">ShdwOffsetX Cell (Page Properties Section)</span></span>

<span data-ttu-id="6a0df-104">図形の影を図形から水平方向にオフセットする場合の距離を、ページの単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="6a0df-104">Determines the distance in page units that a shape's drop shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a0df-105">注釈</span><span class="sxs-lookup"><span data-stu-id="6a0df-105">Remarks</span></span>

<span data-ttu-id="6a0df-p101">この値は、[**ページ設定**] ダイアログ ボックスで設定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] 矢印をクリックします)。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、影のオフセットは変わりません。</span><span class="sxs-lookup"><span data-stu-id="6a0df-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="6a0df-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwOffsetX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6a0df-109">To get a reference to the ShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a0df-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="6a0df-110">Cell name:</span></span>  <br/> | <span data-ttu-id="6a0df-111">ShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="6a0df-111">ShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="6a0df-112">プログラムから、インデックスによって [ShdwOffsetX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6a0df-112">To get a reference to the ShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a0df-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6a0df-113">Section index:</span></span>  <br/> |<span data-ttu-id="6a0df-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6a0df-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6a0df-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6a0df-115">Row index:</span></span>  <br/> |<span data-ttu-id="6a0df-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="6a0df-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="6a0df-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6a0df-117">Cell index:</span></span>  <br/> |<span data-ttu-id="6a0df-118">**visPageShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="6a0df-118">**visPageShdwOffsetX**</span></span> <br/> |
   

