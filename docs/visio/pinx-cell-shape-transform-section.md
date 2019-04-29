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
description: 親図形の原点を基準としたときの、図形の pin (回転の中心) の x 座標を表します。
ms.openlocfilehash: de12b379d5f345209a468298174634ff4f9cd639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404821"
---
# <a name="pinx-cell-shape-transform-section"></a><span data-ttu-id="365d4-103">[PinX] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="365d4-103">PinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="365d4-104">親図形の原点を基準としたときの、図形の pin (回転の中心) の*x*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="365d4-104">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of its parent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="365d4-105">注釈</span><span class="sxs-lookup"><span data-stu-id="365d4-105">Remarks</span></span>

<span data-ttu-id="365d4-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PinX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="365d4-106">To get a reference to the PinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="365d4-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="365d4-107">Cell name:</span></span>  <br/> | <span data-ttu-id="365d4-108">[pinx]</span><span class="sxs-lookup"><span data-stu-id="365d4-108">PinX</span></span>  <br/> |
   
<span data-ttu-id="365d4-109">プログラムから、インデックスによって [PinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="365d4-109">To get a reference to the PinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="365d4-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="365d4-110">Section index:</span></span>  <br/> |<span data-ttu-id="365d4-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="365d4-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="365d4-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="365d4-112">Row index:</span></span>  <br/> |<span data-ttu-id="365d4-113">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="365d4-113">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="365d4-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="365d4-114">Cell index:</span></span>  <br/> |<span data-ttu-id="365d4-115">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="365d4-115">**visXFormPinX**</span></span> <br/> |
   

