---
title: '[LineColor] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: 図形の線の色を指定します。
ms.openlocfilehash: 6086a45108b88475e250c4d833ab4b740f33b8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805705"
---
# <a name="linecolor-cell-line-format-section"></a><span data-ttu-id="1b49b-103">[LineColor] セル ([線の書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="1b49b-103">LineColor Cell (Line Format Section)</span></span>

<span data-ttu-id="1b49b-104">図形の線の色を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b49b-104">Determines the line color of the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1b49b-105">注釈</span><span class="sxs-lookup"><span data-stu-id="1b49b-105">Remarks</span></span>

<span data-ttu-id="1b49b-p101">線の色を設定するには、線の色のコレクション内でインデックスとなっている 0 ～ 23 の数値を入力します。線の色のコレクションは、[**線**] ダイアログ ボックスで参照できます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**太さ**] をポイントして、[**その他の線**] をクリックします)。[LineColor] の値は、[**線**] ダイアログ ボックスで設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="1b49b-p101">To set the line color, enter a number from 0 to 23, which is an index into a collection of line colors. You can view the line color collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**). You can also set the value of LineColor in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="1b49b-109">独自の色を入力するには、RGB または HSL 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b49b-109">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="1b49b-110">その RGB カラーでは、ユーザー設定の色の値と、数値ではなく RGB ( *r, g, b*)、[シェイプ シート] ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1b49b-110">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="1b49b-111">数値演算で使用する場合は、24 以上の値があるユーザー設定の色です。</span><span class="sxs-lookup"><span data-stu-id="1b49b-111">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="1b49b-112">線の色の透過性を設定するには、[LineColorTrans] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="1b49b-112">You can set the transparency of the line color in the LineColorTrans cell.</span></span>
  
<span data-ttu-id="1b49b-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineColor] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b49b-113">To get a reference to the LineColor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b49b-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="1b49b-114">Cell name:</span></span>  <br/> |<span data-ttu-id="1b49b-115">線の色</span><span class="sxs-lookup"><span data-stu-id="1b49b-115">LineColor</span></span>  <br/> |
   
<span data-ttu-id="1b49b-116">プログラムから、インデックスによって [LineColor] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b49b-116">To get a reference to the LineColor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b49b-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1b49b-117">Section index:</span></span>  <br/> |<span data-ttu-id="1b49b-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1b49b-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1b49b-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1b49b-119">Row index:</span></span>  <br/> |<span data-ttu-id="1b49b-120">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="1b49b-120">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="1b49b-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1b49b-121">Cell index:</span></span>  <br/> |<span data-ttu-id="1b49b-122">**visLineColor**</span><span class="sxs-lookup"><span data-stu-id="1b49b-122">**visLineColor**</span></span> <br/> |
   

