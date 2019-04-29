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
ms.openlocfilehash: d0b4ebee6d96bc67c9ca45e8a6194cb91ed6c7f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416938"
---
# <a name="linecolor-cell-line-format-section"></a><span data-ttu-id="e4d99-103">[LineColor] セル ([Line Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="e4d99-103">LineColor Cell (Line Format Section)</span></span>

<span data-ttu-id="e4d99-104">図形の線の色を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4d99-104">Determines the line color of the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e4d99-105">注釈</span><span class="sxs-lookup"><span data-stu-id="e4d99-105">Remarks</span></span>

<span data-ttu-id="e4d99-p101">線の色を設定するには、線の色のコレクション内でインデックスとなっている 0 ～ 23 の数値を入力します。線の色のコレクションは、[**線**] ダイアログ ボックスで参照できます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**太さ**] をポイントして、[**その他の線**] をクリックします)。[LineColor] の値は、[**線**] ダイアログ ボックスで設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="e4d99-p101">To set the line color, enter a number from 0 to 23, which is an index into a collection of line colors. You can view the line color collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**). You can also set the value of LineColor in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="e4d99-109">ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="e4d99-109">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="e4d99-110">ユーザー設定の色の値は rgb カラーで、数字ではなく rgb ( *r, g, b*) は [シェイプシート] ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e4d99-110">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="e4d99-111">ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4d99-111">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="e4d99-112">線の色の透過性を設定するには、[LineColorTrans] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="e4d99-112">You can set the transparency of the line color in the LineColorTrans cell.</span></span>
  
<span data-ttu-id="e4d99-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineColor] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e4d99-113">To get a reference to the LineColor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4d99-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="e4d99-114">Cell name:</span></span>  <br/> |<span data-ttu-id="e4d99-115">linecolor]</span><span class="sxs-lookup"><span data-stu-id="e4d99-115">LineColor</span></span>  <br/> |
   
<span data-ttu-id="e4d99-116">プログラムから、インデックスによって [LineColor] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4d99-116">To get a reference to the LineColor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4d99-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e4d99-117">Section index:</span></span>  <br/> |<span data-ttu-id="e4d99-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e4d99-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e4d99-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e4d99-119">Row index:</span></span>  <br/> |<span data-ttu-id="e4d99-120">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="e4d99-120">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="e4d99-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e4d99-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e4d99-122">**visLineColor**</span><span class="sxs-lookup"><span data-stu-id="e4d99-122">**visLineColor**</span></span> <br/> |
   

