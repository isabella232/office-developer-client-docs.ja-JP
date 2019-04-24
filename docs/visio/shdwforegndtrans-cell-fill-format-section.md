---
title: '[ShdwForegndTrans] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
localization_priority: Normal
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: 図形の影に対して、塗りつぶしパターンの前景 (ストローク部分) に適用される色の透過性レベルを指定します。
ms.openlocfilehash: 0ef3ce525edcce4ccd61f36649ead512545eef58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349099"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a><span data-ttu-id="77b78-103">[ShdwForegndTrans] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="77b78-103">ShdwForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="77b78-104">図形の影に対して、塗りつぶしパターンの前景 (ストローク部分) に適用される色の透過性レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="77b78-104">Determines the transparency level for the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
|<span data-ttu-id="77b78-105">**値**</span><span class="sxs-lookup"><span data-stu-id="77b78-105">**Value**</span></span>|<span data-ttu-id="77b78-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="77b78-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="77b78-107">0 ～ 100</span><span class="sxs-lookup"><span data-stu-id="77b78-107">0 - 100</span></span>  <br/> |<span data-ttu-id="77b78-p101">透過性をパーセントで表します。既定値は 0% (完全に不透明) です。</span><span class="sxs-lookup"><span data-stu-id="77b78-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77b78-110">解説</span><span class="sxs-lookup"><span data-stu-id="77b78-110">Remarks</span></span>

<span data-ttu-id="77b78-111">値は、最も近い 0.5% 単位の値に丸められます。</span><span class="sxs-lookup"><span data-stu-id="77b78-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="77b78-112">値 "100%" は完全な透明を表します。</span><span class="sxs-lookup"><span data-stu-id="77b78-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="77b78-113">完全に透明な塗りつぶしが設定された影は、塗りつぶしがないシャドウとして図面ページに表示されますが、ページ上の他のオブジェクトとは、透明度が 0% の場合と同じように操作します。</span><span class="sxs-lookup"><span data-stu-id="77b78-113">Although a shadow that has a completely transparent fill appears the same on the drawing page as a shadow that has no fill, it interacts with other objects on the page in the same ways as if its transparency were 0%.</span></span>
  
<span data-ttu-id="77b78-p103">この値は、[**影**] ダイアログ ボックスのスライダー コントロールを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックして、[**影のオプション**] をクリックします)。この操作で設定される値は、背景と前景の両方に対する影の透過性の値を制御します。これらの値を個別に設定するには、[シェイプシート] ウィンドウでそれぞれの値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77b78-p103">You can also set this value by using the slider control in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**). This value controls the value of both the background and foreground shadow transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="77b78-117">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwForegndTrans] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="77b78-117">To get a reference to the ShdwForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77b78-118">セル名 :</span><span class="sxs-lookup"><span data-stu-id="77b78-118">Cell name:</span></span>  <br/> |<span data-ttu-id="77b78-119">[shdwforegndtrans]</span><span class="sxs-lookup"><span data-stu-id="77b78-119">ShdwForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="77b78-120">プログラムから、インデックスによって [ShdwForegndTrans] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="77b78-120">To get a reference to the ShdwForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77b78-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="77b78-121">Section index:</span></span>  <br/> |<span data-ttu-id="77b78-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="77b78-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="77b78-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="77b78-123">Row index:</span></span>  <br/> |<span data-ttu-id="77b78-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="77b78-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="77b78-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="77b78-125">Cell index:</span></span>  <br/> |<span data-ttu-id="77b78-126">**visFillShdwForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="77b78-126">**visFillShdwForegndTrans**</span></span> <br/> |
   

