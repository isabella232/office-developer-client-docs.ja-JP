---
title: '[FillBkgndTrans] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253230
localization_priority: Normal
ms.assetid: 87065350-ba9a-aae8-47f6-f263f6700d08
description: 図形の塗りつぶしのパターンに対して、背景 (塗りつぶし部分) に適用される透過性レベルを指定します。
ms.openlocfilehash: c8dcec8cc0bdb87700bb85754298ec4755bae7d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805378"
---
# <a name="fillbkgndtrans-cell-fill-format-section"></a><span data-ttu-id="002a0-103">[FillBkgndTrans] セル ([塗りつぶしの書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="002a0-103">FillBkgndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="002a0-104">図形の塗りつぶしのパターンに対して、背景 (塗りつぶし部分) に適用される透過性レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="002a0-104">Determines the transparency level for the background (fill) color of the shape's fill pattern.</span></span>
  
|<span data-ttu-id="002a0-105">**値**</span><span class="sxs-lookup"><span data-stu-id="002a0-105">**Value**</span></span>|<span data-ttu-id="002a0-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="002a0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="002a0-107">
          0 ～ 100
</span><span class="sxs-lookup"><span data-stu-id="002a0-107">0 - 100</span></span>  <br/> |<span data-ttu-id="002a0-p101">透過性をパーセントで表します。既定値は 0% (完全に不透明) です。</span><span class="sxs-lookup"><span data-stu-id="002a0-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="002a0-110">注釈</span><span class="sxs-lookup"><span data-stu-id="002a0-110">Remarks</span></span>

<span data-ttu-id="002a0-p102">値は、最も近い 0.5% 単位の値に丸められます。値 100% は完全な透明を表します。塗りつぶしが完全に透明な図形は、図面ページでは塗りつぶしがない図形と同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。</span><span class="sxs-lookup"><span data-stu-id="002a0-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent fill appears the same as a shape with no fill on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span>
  
<span data-ttu-id="002a0-p103">この値は、[**塗りつぶし**] ダイアログ ボックスのスライダー コントロールを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**塗りつぶし**] をクリックして、[**塗りつぶしのオプション**] をクリックします)。この値は、前景と背景の両方に対する塗りつぶしの透過性を制御します。これらの値を個別に設定するには、[シェイプシート] ウィンドウでそれぞれの値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="002a0-p103">You can also set this value using the slider control in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**). This value controls the value of both the background and foreground fill transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="002a0-117">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FillBkgndTrans] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="002a0-117">To get a reference to the FillBkgndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="002a0-118">セル名:</span><span class="sxs-lookup"><span data-stu-id="002a0-118">Cell name:</span></span>  <br/> |<span data-ttu-id="002a0-119">FillBkgndTrans</span><span class="sxs-lookup"><span data-stu-id="002a0-119">FillBkgndTrans</span></span>  <br/> |
   
<span data-ttu-id="002a0-120">プログラムから、インデックスによって [FillBkgndTrans] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="002a0-120">To get a reference to the FillBkgndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="002a0-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="002a0-121">Section index:</span></span>  <br/> |<span data-ttu-id="002a0-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="002a0-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="002a0-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="002a0-123">Row index:</span></span>  <br/> |<span data-ttu-id="002a0-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="002a0-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="002a0-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="002a0-125">Cell index:</span></span>  <br/> |<span data-ttu-id="002a0-126">**visFillBkgndTrans**</span><span class="sxs-lookup"><span data-stu-id="002a0-126">**visFillBkgndTrans**</span></span> <br/> |
   

