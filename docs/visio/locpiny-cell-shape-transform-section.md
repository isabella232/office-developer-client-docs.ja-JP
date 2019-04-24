---
title: '[LocPinY] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 図形の原点を基準としたときの、図形の pin (回転の中心) の y 座標を表します。 [LocPinY] を決定する既定の数式は次のとおりです。
ms.openlocfilehash: e65bfec8fdcf2be1ee92c23b7afcb183c95ea9fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358045"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="71750-104">[LocPinY] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="71750-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="71750-105">図形の原点を基準としたときの、図形の pin (回転の中心) の*y*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="71750-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="71750-106">[LocPinY] を決定する既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="71750-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="71750-107">= 高さ\* 0.5</span><span class="sxs-lookup"><span data-stu-id="71750-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="71750-108">解説</span><span class="sxs-lookup"><span data-stu-id="71750-108">Remarks</span></span>

<span data-ttu-id="71750-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LocPinY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="71750-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71750-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="71750-110">Cell name:</span></span>  <br/> | <span data-ttu-id="71750-111">[locpiny]</span><span class="sxs-lookup"><span data-stu-id="71750-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="71750-112">プログラムから、インデックスによって [LocPinY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="71750-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71750-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="71750-113">Section index:</span></span>  <br/> |<span data-ttu-id="71750-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="71750-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="71750-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="71750-115">Row index:</span></span>  <br/> |<span data-ttu-id="71750-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="71750-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="71750-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="71750-117">Cell index:</span></span>  <br/> |<span data-ttu-id="71750-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="71750-118">**visXFormLocPinY**</span></span> <br/> |
   

