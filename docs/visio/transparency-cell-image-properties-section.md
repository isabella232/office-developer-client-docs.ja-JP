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
# <a name="transparency-cell-image-properties-section"></a><span data-ttu-id="eb6ec-103">[Transparency] セル ([Image Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="eb6ec-103">Transparency Cell (Image Properties Section)</span></span>

<span data-ttu-id="eb6ec-104">レイヤーの色の透過性レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="eb6ec-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="eb6ec-105">**値**</span><span class="sxs-lookup"><span data-stu-id="eb6ec-105">**Value**</span></span>|<span data-ttu-id="eb6ec-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="eb6ec-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb6ec-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="eb6ec-107">0 - 100</span></span>  <br/> |<span data-ttu-id="eb6ec-p101">透過性をパーセントで表します。既定値は 0% (完全に不透明) です。</span><span class="sxs-lookup"><span data-stu-id="eb6ec-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb6ec-110">注釈</span><span class="sxs-lookup"><span data-stu-id="eb6ec-110">Remarks</span></span>

<span data-ttu-id="eb6ec-111">値は、最も近い 0.5% に丸められます。</span><span class="sxs-lookup"><span data-stu-id="eb6ec-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="eb6ec-112">100% の値は、完全に透過的です。</span><span class="sxs-lookup"><span data-stu-id="eb6ec-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="eb6ec-113">完全に透明な色を持つレイヤーは、レイヤーの色がないと図面ページ上で同じように表示されますとの対話ページ上の他のオブジェクトと同様に、透過性が 0% であるかのようです。</span><span class="sxs-lookup"><span data-stu-id="eb6ec-113">Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span> <span data-ttu-id="eb6ec-114">**[レイヤー プロパティ**] ダイアログ ボックスで、スライダーのつまみを使用してこの値を設定することもできます ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="eb6ec-114">You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="eb6ec-115">別の数式または**CellsU**プロパティを使用したプログラムから、[透過性] セルへの参照を名前によって取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="eb6ec-115">To get a reference to the Transparency cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb6ec-116">セル名 :</span><span class="sxs-lookup"><span data-stu-id="eb6ec-116">Cell name:</span></span>  <br/> |<span data-ttu-id="eb6ec-117">Transparency</span><span class="sxs-lookup"><span data-stu-id="eb6ec-117">Transparency</span></span>  <br/> |
   
<span data-ttu-id="eb6ec-118">プログラムから、インデックスによって [透過性] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="eb6ec-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb6ec-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb6ec-119">Section index:</span></span>  <br/> |<span data-ttu-id="eb6ec-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eb6ec-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="eb6ec-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb6ec-121">Row index:</span></span>  <br/> |<span data-ttu-id="eb6ec-122">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="eb6ec-122">**visRowImage**</span></span> <br/> |
|<span data-ttu-id="eb6ec-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="eb6ec-123">Cell index:</span></span>  <br/> |<span data-ttu-id="eb6ec-124">**visImageTransparency**</span><span class="sxs-lookup"><span data-stu-id="eb6ec-124">**visImageTransparency**</span></span> <br/> |
   

