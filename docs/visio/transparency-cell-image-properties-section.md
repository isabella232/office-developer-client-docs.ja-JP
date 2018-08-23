---
title: '[Transparency] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: レイヤーの色の透過性レベルを指定します。
ms.openlocfilehash: 5537cbdcd49c66f3bc28a58051f6e2888a290cd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806676"
---
# <a name="transparency-cell-image-properties-section"></a><span data-ttu-id="ae4c1-103">[Transparency ] セル ([画像のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="ae4c1-103">Transparency Cell (Image Properties Section)</span></span>

<span data-ttu-id="ae4c1-104">レイヤーの色の透過性レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="ae4c1-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="ae4c1-105">**値**</span><span class="sxs-lookup"><span data-stu-id="ae4c1-105">**Value**</span></span>|<span data-ttu-id="ae4c1-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="ae4c1-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae4c1-107">
          0 ～ 100
</span><span class="sxs-lookup"><span data-stu-id="ae4c1-107">0 - 100</span></span>  <br/> |<span data-ttu-id="ae4c1-p101">透過性をパーセントで表します。既定値は 0% (完全に不透明) です。</span><span class="sxs-lookup"><span data-stu-id="ae4c1-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae4c1-110">注釈</span><span class="sxs-lookup"><span data-stu-id="ae4c1-110">Remarks</span></span>

<span data-ttu-id="ae4c1-p102">値は、最も近い 0.5% 単位の値に丸められます。値 "100%" は完全な透明を表します。完全に透明な色のレイヤーは図面ページでは無色のレイヤーと同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。この値は、[**レイヤー プロパティ**] ダイアログ ボックスのスライダー コントロールを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックして、[**レイヤー プロパティ**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="ae4c1-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%. You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="ae4c1-115">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Transparency] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae4c1-115">To get a reference to the Transparency cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae4c1-116">セル名 :</span><span class="sxs-lookup"><span data-stu-id="ae4c1-116">Cell name:</span></span>  <br/> |<span data-ttu-id="ae4c1-117">Transparency</span><span class="sxs-lookup"><span data-stu-id="ae4c1-117">Transparency</span></span>  <br/> |
   
<span data-ttu-id="ae4c1-118">プログラムから、インデックスによって [Transparency] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae4c1-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae4c1-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae4c1-119">Section index:</span></span>  <br/> |<span data-ttu-id="ae4c1-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ae4c1-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ae4c1-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae4c1-121">Row index:</span></span>  <br/> |<span data-ttu-id="ae4c1-122">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="ae4c1-122">**visRowImage**</span></span> <br/> |
|<span data-ttu-id="ae4c1-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ae4c1-123">Cell index:</span></span>  <br/> |<span data-ttu-id="ae4c1-124">**visImageTransparency**</span><span class="sxs-lookup"><span data-stu-id="ae4c1-124">**visImageTransparency**</span></span> <br/> |
   

