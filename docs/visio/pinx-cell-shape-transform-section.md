---
title: '[PinX] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm790
localization_priority: Normal
ms.assetid: dd88fb8d-3ec3-476a-870d-6642b191496f
description: X を表しますが、親の原点を基準として、図形の pin (回転の中心) の座標。
ms.openlocfilehash: 74e98732f1e0c44fa20c159070198ed4f98cee92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805983"
---
# <a name="pinx-cell-shape-transform-section"></a><span data-ttu-id="241b3-103">[PinX] セル ([図形変換] セクション)</span><span class="sxs-lookup"><span data-stu-id="241b3-103">PinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="241b3-104">*X*を表しますが、親の原点を基準として、図形の pin (回転の中心) の座標。</span><span class="sxs-lookup"><span data-stu-id="241b3-104">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of its parent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="241b3-105">注釈</span><span class="sxs-lookup"><span data-stu-id="241b3-105">Remarks</span></span>

<span data-ttu-id="241b3-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PinX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="241b3-106">To get a reference to the PinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="241b3-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="241b3-107">Cell name:</span></span>  <br/> | <span data-ttu-id="241b3-108">[Pinx]</span><span class="sxs-lookup"><span data-stu-id="241b3-108">PinX</span></span>  <br/> |
   
<span data-ttu-id="241b3-109">プログラムから、インデックスによって [PinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="241b3-109">To get a reference to the PinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="241b3-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="241b3-110">Section index:</span></span>  <br/> |<span data-ttu-id="241b3-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="241b3-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="241b3-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="241b3-112">Row index:</span></span>  <br/> |<span data-ttu-id="241b3-113">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="241b3-113">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="241b3-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="241b3-114">Cell index:</span></span>  <br/> |<span data-ttu-id="241b3-115">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="241b3-115">**visXFormPinX**</span></span> <br/> |
   

