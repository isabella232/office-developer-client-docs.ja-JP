---
title: '[FillBkgnd] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: 図形の塗りつぶしのパターンで背景に使用する色 (塗りつぶし部分) を指定します。
ms.openlocfilehash: d1222026887313d7737a3a0ded9e798e9bf5ea30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805371"
---
# <a name="fillbkgnd-cell-fill-format-section"></a><span data-ttu-id="15bd3-103">[FillBkgnd] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="15bd3-103">FillBkgnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="15bd3-104">図形の塗りつぶしのパターンで背景に使用する色 (塗りつぶし部分) を指定します。</span><span class="sxs-lookup"><span data-stu-id="15bd3-104">Determines the color used for the background (fill) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="15bd3-105">注釈</span><span class="sxs-lookup"><span data-stu-id="15bd3-105">Remarks</span></span>

<span data-ttu-id="15bd3-106">色を設定するには、0 ～ 23 の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="15bd3-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="15bd3-107">独自の色を入力するには、RGB または HSL 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="15bd3-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="15bd3-108">その RGB カラーでは、ユーザー設定の色の値と、数値ではなく RGB (*r, g, b*)、[シェイプ シート] ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="15bd3-108">The value of a custom color is its RGB color, and RGB(*r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="15bd3-109">数値演算で使用する場合は、24 以上の値があるユーザー設定の色です。</span><span class="sxs-lookup"><span data-stu-id="15bd3-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="15bd3-110">背景の塗りつぶしの色に関する透過性を設定するには、[FillBkgndTrans] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="15bd3-110">You can set the transparency of the background fill in the FillBkgndTrans cell.</span></span> 
  
<span data-ttu-id="15bd3-111">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [fillbkgnd] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="15bd3-111">To get a reference to the FillBkgnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="15bd3-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="15bd3-112">Cell name:</span></span>  <br/> | <span data-ttu-id="15bd3-113">[Fillbkgnd]</span><span class="sxs-lookup"><span data-stu-id="15bd3-113">FillBkgnd</span></span>  <br/> |
   
<span data-ttu-id="15bd3-114">プログラムから、インデックスによって [fillbkgnd] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="15bd3-114">To get a reference to the FillBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="15bd3-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="15bd3-115">Section index:</span></span>  <br/> |<span data-ttu-id="15bd3-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="15bd3-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="15bd3-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="15bd3-117">Row index:</span></span>  <br/> |<span data-ttu-id="15bd3-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="15bd3-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="15bd3-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="15bd3-119">Cell index:</span></span>  <br/> |<span data-ttu-id="15bd3-120">**visFillBkgnd**</span><span class="sxs-lookup"><span data-stu-id="15bd3-120">**visFillBkgnd**</span></span> <br/> |
   

