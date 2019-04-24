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
ms.openlocfilehash: 555ea15de0279a37bcf67de7374d922b8692ce02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359298"
---
# <a name="linecolortrans-cell-line-format-section"></a><span data-ttu-id="8adb1-103">[LineColorTrans] セル ([Line Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="8adb1-103">LineColorTrans Cell (Line Format Section)</span></span>

<span data-ttu-id="8adb1-104">図形の線の色の透過性レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="8adb1-104">Determines the transparency level of a shape's line color.</span></span>
  
|<span data-ttu-id="8adb1-105">**値**</span><span class="sxs-lookup"><span data-stu-id="8adb1-105">**Value**</span></span>|<span data-ttu-id="8adb1-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="8adb1-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8adb1-107">0 ～ 100</span><span class="sxs-lookup"><span data-stu-id="8adb1-107">0 - 100</span></span>  <br/> |<span data-ttu-id="8adb1-p101">透過性をパーセントで表します。既定値は 0% (完全に不透明) です。</span><span class="sxs-lookup"><span data-stu-id="8adb1-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8adb1-110">解説</span><span class="sxs-lookup"><span data-stu-id="8adb1-110">Remarks</span></span>

<span data-ttu-id="8adb1-p102">値は、最も近い 0.5% 単位の値に丸められます。値 "100%" は完全な透明を表します。完全に透明な色の線をもつ図形は、図面ページでは線がない図形と同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。</span><span class="sxs-lookup"><span data-stu-id="8adb1-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent line color appears the same as a shape with no lines on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span> 
  
<span data-ttu-id="8adb1-114">この値は、[**線**] ダイアログ ボックスのスライダー コントロールを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**太さ**] をポイントして、[**その他の線**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="8adb1-114">You can also set this value by using the slider control in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="8adb1-115">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineColorTrans] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8adb1-115">To get a reference to the LineColorTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8adb1-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="8adb1-116">Cell name:</span></span>  <br/> |<span data-ttu-id="8adb1-117">[linecolortrans]</span><span class="sxs-lookup"><span data-stu-id="8adb1-117">LineColorTrans</span></span>  <br/> |
   
<span data-ttu-id="8adb1-118">プログラムから、インデックスによって [LineColorTrans] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8adb1-118">To get a reference to the LineColorTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8adb1-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8adb1-119">Section index:</span></span>  <br/> |<span data-ttu-id="8adb1-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8adb1-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8adb1-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8adb1-121">Row index:</span></span>  <br/> |<span data-ttu-id="8adb1-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="8adb1-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="8adb1-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8adb1-123">Cell index:</span></span>  <br/> |<span data-ttu-id="8adb1-124">**visLineColorTrans**</span><span class="sxs-lookup"><span data-stu-id="8adb1-124">**visLineColorTrans**</span></span> <br/> |
   

