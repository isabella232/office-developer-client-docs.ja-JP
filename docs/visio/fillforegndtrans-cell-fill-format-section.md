---
title: '[FillForegndTrans] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253231
localization_priority: Normal
ms.assetid: 8b1b3904-6635-3fd1-31a9-ff32c19394af
description: 図形の塗りつぶしのパターンに対して、前景 (ストローク部分) に適用される透過性レベルを指定します。
ms.openlocfilehash: d05a83f83ea3d95ac3d42a2bfb3996917119f580
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427851"
---
# <a name="fillforegndtrans-cell-fill-format-section"></a><span data-ttu-id="41427-103">[FillForegndTrans] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="41427-103">FillForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="41427-104">図形の塗りつぶしのパターンに対して、前景 (ストローク部分) に適用される透過性レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="41427-104">Determines the transparency level for the foreground (fill) color of the shape's fill pattern.</span></span>
  
|<span data-ttu-id="41427-105">**値**</span><span class="sxs-lookup"><span data-stu-id="41427-105">**Value**</span></span>|<span data-ttu-id="41427-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="41427-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41427-107">0 ～ 100</span><span class="sxs-lookup"><span data-stu-id="41427-107">0 - 100</span></span>  <br/> |<span data-ttu-id="41427-p101">透過性をパーセントで表します。既定値は 0% (完全に不透明) です。</span><span class="sxs-lookup"><span data-stu-id="41427-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41427-110">注釈</span><span class="sxs-lookup"><span data-stu-id="41427-110">Remarks</span></span>

<span data-ttu-id="41427-p102">値は、最も近い 0.5% 単位の値に丸められます。値 100% は完全な透明を表します。塗りつぶしが完全に透明な図形は、図面ページでは塗りつぶしがない図形と同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。</span><span class="sxs-lookup"><span data-stu-id="41427-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent fill appears the same as a shape with no fill on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span>
  
<span data-ttu-id="41427-p103">この値は、[**塗りつぶし**] ダイアログ ボックスのスライダー コントロールを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**塗りつぶし**] をクリックして、[**塗りつぶしのオプション**] をクリックします)。この値は、前景と背景の両方に対する塗りつぶしの透過性を制御します。これらの値を個別に設定するには、[シェイプシート] ウィンドウでそれぞれの値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41427-p103">You can also set this value using the slider control in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**). This value controls the value of both the background and foreground fill transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="41427-117">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FillForegndTrans] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="41427-117">To get a reference to the FillForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41427-118">セル名:</span><span class="sxs-lookup"><span data-stu-id="41427-118">Cell name:</span></span>  <br/> |<span data-ttu-id="41427-119">FillForegndTrans</span><span class="sxs-lookup"><span data-stu-id="41427-119">FillForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="41427-120">プログラムから、インデックスによって [FillForegndTrans] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="41427-120">To get a reference to the FillForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41427-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="41427-121">Section index:</span></span>  <br/> |<span data-ttu-id="41427-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="41427-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="41427-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="41427-123">Row index:</span></span>  <br/> |<span data-ttu-id="41427-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="41427-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="41427-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="41427-125">Cell index:</span></span>  <br/> |<span data-ttu-id="41427-126">**visFillForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="41427-126">**visFillForegndTrans**</span></span> <br/> |
   

