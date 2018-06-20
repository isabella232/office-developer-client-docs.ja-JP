---
title: '[LineColorTrans] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
localization_priority: Normal
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: 図形の線の色の透過性レベルを指定します。
ms.openlocfilehash: 81c23b77c4663158819f9d5fe53765860183e039
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805702"
---
# <a name="linecolortrans-cell-line-format-section"></a><span data-ttu-id="1bd8b-103">[LineColorTrans] セル ([Line Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="1bd8b-103">LineColorTrans Cell (Line Format Section)</span></span>

<span data-ttu-id="1bd8b-104">図形の線の色の透過性レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="1bd8b-104">Determines the transparency level of a shape's line color.</span></span>
  
|<span data-ttu-id="1bd8b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="1bd8b-105">**Value**</span></span>|<span data-ttu-id="1bd8b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="1bd8b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1bd8b-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="1bd8b-107">0 - 100</span></span>  <br/> |<span data-ttu-id="1bd8b-p101">透過性をパーセントで表します。既定値は 0% (完全に不透明) です。</span><span class="sxs-lookup"><span data-stu-id="1bd8b-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bd8b-110">注釈</span><span class="sxs-lookup"><span data-stu-id="1bd8b-110">Remarks</span></span>

<span data-ttu-id="1bd8b-p102">値は、最も近い 0.5% 単位の値に丸められます。値 "100%" は完全な透明を表します。完全に透明な色の線をもつ図形は、図面ページでは線がない図形と同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。</span><span class="sxs-lookup"><span data-stu-id="1bd8b-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent line color appears the same as a shape with no lines on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span> 
  
<span data-ttu-id="1bd8b-114">**線**] ダイアログ ボックスのスライダー コントロールを使用してこの値を設定することもできます ([**ホーム**] タブの [**図形**] グループで、[**行**] をクリックして、[**太さ**] をポイントおよび**他の線**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="1bd8b-114">You can also set this value by using the slider control in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="1bd8b-115">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineColorTrans] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd8b-115">To get a reference to the LineColorTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1bd8b-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="1bd8b-116">Cell name:</span></span>  <br/> |<span data-ttu-id="1bd8b-117">LineColorTrans</span><span class="sxs-lookup"><span data-stu-id="1bd8b-117">LineColorTrans</span></span>  <br/> |
   
<span data-ttu-id="1bd8b-118">プログラムから、インデックスによって [LineColorTrans] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd8b-118">To get a reference to the LineColorTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1bd8b-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1bd8b-119">Section index:</span></span>  <br/> |<span data-ttu-id="1bd8b-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1bd8b-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1bd8b-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1bd8b-121">Row index:</span></span>  <br/> |<span data-ttu-id="1bd8b-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="1bd8b-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="1bd8b-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1bd8b-123">Cell index:</span></span>  <br/> |<span data-ttu-id="1bd8b-124">**visLineColorTrans**</span><span class="sxs-lookup"><span data-stu-id="1bd8b-124">**visLineColorTrans**</span></span> <br/> |
   

