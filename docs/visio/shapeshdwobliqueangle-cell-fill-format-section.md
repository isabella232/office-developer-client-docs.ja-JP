---
title: '[ShapeShdwObliqueAngle] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033174
localization_priority: Normal
ms.assetid: bad4c512-e91f-d459-d65c-a4ab725c3c14
description: 図形の斜体の影に角度を指定します。
ms.openlocfilehash: 005415e497a4d985d3fb8ec70d62ba40d9e80c91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349195"
---
# <a name="shapeshdwobliqueangle-cell-fill-format-section"></a><span data-ttu-id="d7e72-103">[ShapeShdwObliqueAngle] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="d7e72-103">ShapeShdwObliqueAngle Cell (Fill Format Section)</span></span>

<span data-ttu-id="d7e72-104">図形の斜体の影に角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7e72-104">Specifies the angle of oblique direction of a shape's shadow.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7e72-105">解説</span><span class="sxs-lookup"><span data-stu-id="d7e72-105">Remarks</span></span>

<span data-ttu-id="d7e72-106">このセルの値がゼロ (0) の場合は影の傾きの角度が真上で、時計回りに角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7e72-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
<span data-ttu-id="d7e72-107">この値は、[**影**] ダイアログ ボックスの [**方向**] 設定の値に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックし、[**影のオプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="d7e72-107">This value corresponds to the value of the **Direction** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="d7e72-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeShdwObliqueAngle] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d7e72-108">To get a reference to the ShapeShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7e72-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="d7e72-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d7e72-110">[shapeshdwobliqueangle]</span><span class="sxs-lookup"><span data-stu-id="d7e72-110">ShapeShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="d7e72-111">プログラムから、インデックスによって [ShapeShdwObliqueAngle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7e72-111">To get a reference to the ShapeShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7e72-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d7e72-112">Section index:</span></span>  <br/> |<span data-ttu-id="d7e72-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d7e72-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d7e72-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d7e72-114">Row index:</span></span>  <br/> |<span data-ttu-id="d7e72-115">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="d7e72-115">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="d7e72-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d7e72-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d7e72-117">**visFillShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="d7e72-117">**visFillShdwObliqueAngle**</span></span> <br/> |
   

