---
title: '[FillForegnd] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: 図形の塗りつぶしのパターンで前景 (ストローク部分) に使用する色を指定します。
ms.openlocfilehash: 352fecf8d99069cfb5ebd72d295284dc03446364
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322506"
---
# <a name="fillforegnd-cell-fill-format-section"></a><span data-ttu-id="981d0-103">[FillForegnd] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="981d0-103">FillForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="981d0-104">図形の塗りつぶしのパターンで前景 (ストローク部分) に使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="981d0-104">Determines the color used for the foreground (stroke) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="981d0-105">解説</span><span class="sxs-lookup"><span data-stu-id="981d0-105">Remarks</span></span>

<span data-ttu-id="981d0-106">色を設定するには、0 ～ 23 の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="981d0-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="981d0-107">ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="981d0-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="981d0-108">ユーザー設定の色の値は rgb カラーで、数字ではなく rgb ( *r, g, b*) は [シェイプシート] ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="981d0-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="981d0-109">ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="981d0-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="981d0-110">前景の塗りつぶしの色に関する透過性を設定するには、[FillForegndTrans] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="981d0-110">You can set the transparency of the foreground fill in the FillForegndTrans cell.</span></span>
  
<span data-ttu-id="981d0-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FillForegnd] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="981d0-111">To get a reference to the FillForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="981d0-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="981d0-112">Cell name:</span></span>  <br/> |<span data-ttu-id="981d0-113">[fillforegnd]</span><span class="sxs-lookup"><span data-stu-id="981d0-113">FillForegnd</span></span>  <br/> |
   
<span data-ttu-id="981d0-114">プログラムから、インデックスによって [FillForegnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="981d0-114">To get a reference to the FillForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="981d0-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="981d0-115">Section index:</span></span>  <br/> |<span data-ttu-id="981d0-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="981d0-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="981d0-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="981d0-117">Row index:</span></span>  <br/> |<span data-ttu-id="981d0-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="981d0-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="981d0-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="981d0-119">Cell index:</span></span>  <br/> |<span data-ttu-id="981d0-120">**visFillForegnd**</span><span class="sxs-lookup"><span data-stu-id="981d0-120">**visFillForegnd**</span></span> <br/> |
   

