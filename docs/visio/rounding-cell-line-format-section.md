---
title: '[Rounding] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: 1 つのパス上で接する 2 つの連続したセグメントに適用される、円弧の半径を示します。たとえば、このセルを使用すると、四角形の角を丸くできます。丸みを設定するには、値と単位を入力します (数値と単位を組み合わせる)。
ms.openlocfilehash: d64d3266e3dd2b0a3998955efe271aab04905fbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358584"
---
# <a name="rounding-cell-line-format-section"></a><span data-ttu-id="de2b9-105">[Rounding] セル ([Line Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="de2b9-105">Rounding Cell (Line Format Section)</span></span>

<span data-ttu-id="de2b9-p102">1 つのパス上で接する 2 つの連続したセグメントに適用される、円弧の半径を示します。たとえば、このセルを使用すると、四角形の角を丸くできます。丸みを設定するには、値と単位を入力します (数値と単位を組み合わせる)。</span><span class="sxs-lookup"><span data-stu-id="de2b9-p102">Indicates the radius of the rounding arc applied where two contiguous segments of a path meet. For example, rounding can be used to give a rectangle rounded corners. To set rounding, enter a value with units of measure (a number-unit pair).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="de2b9-109">解説</span><span class="sxs-lookup"><span data-stu-id="de2b9-109">Remarks</span></span>

<span data-ttu-id="de2b9-110">この値は、[**線**] ダイアログボックスで設定することもできます ([**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**太さ**] をポイントして、[**その他の線**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="de2b9-110">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="de2b9-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Rounding] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="de2b9-111">To get a reference to the Rounding cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de2b9-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="de2b9-112">Cell name:</span></span>  <br/> |<span data-ttu-id="de2b9-113">丸めの方法</span><span class="sxs-lookup"><span data-stu-id="de2b9-113">Rounding</span></span>  <br/> |
   
<span data-ttu-id="de2b9-114">プログラムから、インデックスによって [Rounding] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="de2b9-114">To get a reference to the Rounding cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de2b9-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="de2b9-115">Section index:</span></span>  <br/> |<span data-ttu-id="de2b9-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="de2b9-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="de2b9-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="de2b9-117">Row index:</span></span>  <br/> |<span data-ttu-id="de2b9-118">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="de2b9-118">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="de2b9-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="de2b9-119">Cell index:</span></span>  <br/> |<span data-ttu-id="de2b9-120">**visLineRounding**</span><span class="sxs-lookup"><span data-stu-id="de2b9-120">**visLineRounding**</span></span> <br/> |
   

