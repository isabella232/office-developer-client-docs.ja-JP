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
ms.openlocfilehash: 5fd385fc2f46f1ff8eedc961833813ec16ba7b73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806448"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a><span data-ttu-id="b1fe4-103">[ShdwForegndTrans] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="b1fe4-103">ShdwForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="b1fe4-104">図形の影に対して、塗りつぶしパターンの前景 (ストローク部分) に適用される色の透過性レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="b1fe4-104">Determines the transparency level for the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
|<span data-ttu-id="b1fe4-105">**値**</span><span class="sxs-lookup"><span data-stu-id="b1fe4-105">**Value**</span></span>|<span data-ttu-id="b1fe4-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="b1fe4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1fe4-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="b1fe4-107">0 - 100</span></span>  <br/> |<span data-ttu-id="b1fe4-p101">透過性をパーセントで表します。既定値は 0% (完全に不透明) です。</span><span class="sxs-lookup"><span data-stu-id="b1fe4-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1fe4-110">注釈</span><span class="sxs-lookup"><span data-stu-id="b1fe4-110">Remarks</span></span>

<span data-ttu-id="b1fe4-111">値は、最も近い 0.5% に丸められます。</span><span class="sxs-lookup"><span data-stu-id="b1fe4-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="b1fe4-112">100% の値は、完全に透過的です。</span><span class="sxs-lookup"><span data-stu-id="b1fe4-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="b1fe4-113">完全に透明な塗りつぶしが設定されている影は、塗りつぶしがない影と図面ページ上で同じように表示されますとの対話のページで他のオブジェクトと同じ方法で、透過性が 0% であるかのようです。</span><span class="sxs-lookup"><span data-stu-id="b1fe4-113">Although a shadow that has a completely transparent fill appears the same on the drawing page as a shadow that has no fill, it interacts with other objects on the page in the same ways as if its transparency were 0%.</span></span>
  
<span data-ttu-id="b1fe4-114">[**影**] ダイアログ ボックスで、スライダーのつまみを使用してこの値を設定することもできます ([**ホーム**] タブの [**図形**] グループで、**シャドウ**] をクリックし、[**影のオプション**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="b1fe4-114">You can also set this value by using the slider control in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span> <span data-ttu-id="b1fe4-115">この値は、前景色と背景の両方の影の透明度の値を制御します。</span><span class="sxs-lookup"><span data-stu-id="b1fe4-115">This value controls the value of both the background and foreground shadow transparencies.</span></span> <span data-ttu-id="b1fe4-116">これらの値を個別に設定するのには、シェイプ シート ウィンドウで入力にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1fe4-116">To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="b1fe4-117">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShdwForegndTrans] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="b1fe4-117">To get a reference to the ShdwForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1fe4-118">セル名 :</span><span class="sxs-lookup"><span data-stu-id="b1fe4-118">Cell name:</span></span>  <br/> |<span data-ttu-id="b1fe4-119">ShdwForegndTrans</span><span class="sxs-lookup"><span data-stu-id="b1fe4-119">ShdwForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="b1fe4-120">プログラムから、インデックスによって [ShdwForegndTrans] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="b1fe4-120">To get a reference to the ShdwForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1fe4-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1fe4-121">Section index:</span></span>  <br/> |<span data-ttu-id="b1fe4-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b1fe4-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b1fe4-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1fe4-123">Row index:</span></span>  <br/> |<span data-ttu-id="b1fe4-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="b1fe4-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="b1fe4-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1fe4-125">Cell index:</span></span>  <br/> |<span data-ttu-id="b1fe4-126">**visFillShdwForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="b1fe4-126">**visFillShdwForegndTrans**</span></span> <br/> |
   

