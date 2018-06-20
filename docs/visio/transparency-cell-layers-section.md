---
title: '[Transparency] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
localization_priority: Normal
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: レイヤーの色の透過性レベルを指定します。
ms.openlocfilehash: 7c205612436e7731f268e17c851616beebf809dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806682"
---
# <a name="transparency-cell-layers-section"></a><span data-ttu-id="b1d94-103">[Transparency] セル ([Layers] セクション)</span><span class="sxs-lookup"><span data-stu-id="b1d94-103">Transparency Cell (Layers Section)</span></span>

<span data-ttu-id="b1d94-104">レイヤーの色の透過性レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="b1d94-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="b1d94-105">**値**</span><span class="sxs-lookup"><span data-stu-id="b1d94-105">**Value**</span></span>|<span data-ttu-id="b1d94-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="b1d94-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1d94-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="b1d94-107">0 - 100</span></span>  <br/> |<span data-ttu-id="b1d94-p101">透過性をパーセントで表します。既定値は 0% (完全に不透明) です。</span><span class="sxs-lookup"><span data-stu-id="b1d94-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1d94-110">注釈</span><span class="sxs-lookup"><span data-stu-id="b1d94-110">Remarks</span></span>

<span data-ttu-id="b1d94-111">値は、最も近い 0.5% に丸められます。</span><span class="sxs-lookup"><span data-stu-id="b1d94-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="b1d94-112">100% の値は、完全に透過的です。</span><span class="sxs-lookup"><span data-stu-id="b1d94-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="b1d94-113">完全に透明な色を持つレイヤーは、レイヤーの色がないと図面ページ上で同じように表示されますとの対話ページ上の他のオブジェクトと同様に、透過性が 0% であるかのようです。</span><span class="sxs-lookup"><span data-stu-id="b1d94-113">Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span> <span data-ttu-id="b1d94-114">**[レイヤー プロパティ**] ダイアログ ボックスで、スライダーのつまみを使用してこの値を設定することもできます ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="b1d94-114">You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="b1d94-115">参照を取得する透明のセルに名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b1d94-115">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1d94-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="b1d94-116">Cell name:</span></span>  <br/> |<span data-ttu-id="b1d94-117">Layers.ColorTrans [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="b1d94-117">Layers.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b1d94-118">プログラムから、インデックスによって [透過性] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="b1d94-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1d94-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1d94-119">Section index:</span></span>  <br/> |<span data-ttu-id="b1d94-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="b1d94-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="b1d94-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1d94-121">Row index:</span></span>  <br/> |<span data-ttu-id="b1d94-122">**visRowLayer** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="b1d94-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b1d94-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1d94-123">Cell index:</span></span>  <br/> |<span data-ttu-id="b1d94-124">**visLayerColorTrans**</span><span class="sxs-lookup"><span data-stu-id="b1d94-124">**visLayerColorTrans**</span></span> <br/> |
   

