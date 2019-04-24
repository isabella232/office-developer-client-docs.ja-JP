---
title: '[ShapeShdwOffsetY] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60077
localization_priority: Normal
ms.assetid: ef200f41-7b69-1291-f9df-a7035239a033
description: 図形の影を図形から垂直方向にオフセットする距離を、ページの単位で指定します。
ms.openlocfilehash: 4ae4347ba9009e88bbd181d4dd6e242e1fad53be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349141"
---
# <a name="shapeshdwoffsety-cell-fill-format-section"></a><span data-ttu-id="fb83b-103">[ShapeShdwOffsetY] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="fb83b-103">ShapeShdwOffsetY Cell (Fill Format Section)</span></span>

<span data-ttu-id="fb83b-104">図形の影を図形から垂直方向にオフセットする距離を、ページの単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="fb83b-104">Determines the distance in page units that a shape's shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb83b-105">解説</span><span class="sxs-lookup"><span data-stu-id="fb83b-105">Remarks</span></span>

<span data-ttu-id="fb83b-106">この値は、[**影**] ダイアログ ボックスの [**Y オフセット**] 設定の値に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックして、[**影のオプション**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="fb83b-106">This value corresponds to the value in the **Y Offset** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="fb83b-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeShdwOffsetY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fb83b-107">To get a reference to the ShapeShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb83b-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="fb83b-108">Cell name:</span></span>  <br/> | <span data-ttu-id="fb83b-109">[shapeshdwoffsety]</span><span class="sxs-lookup"><span data-stu-id="fb83b-109">ShapeShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="fb83b-110">プログラムから、インデックスによって [ShapeShdwOffsetY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fb83b-110">To get a reference to the ShapeShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb83b-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fb83b-111">Section index:</span></span>  <br/> |<span data-ttu-id="fb83b-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fb83b-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fb83b-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fb83b-113">Row index:</span></span>  <br/> |<span data-ttu-id="fb83b-114">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="fb83b-114">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="fb83b-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fb83b-115">Cell index:</span></span>  <br/> |<span data-ttu-id="fb83b-116">**visFillShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="fb83b-116">**visFillShdwOffsetY**</span></span> <br/> |
   

