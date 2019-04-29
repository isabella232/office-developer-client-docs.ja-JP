---
title: '[PinY] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm795
localization_priority: Normal
ms.assetid: 98b86b9d-9cc0-1169-1c44-ef1505bf92fa
description: 親図形の原点を基準としたときの、図形の pin (回転の中心) の y 座標を表します。
ms.openlocfilehash: 17daf691e4802a93775bfd5272d2142ef33bd189
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411863"
---
# <a name="piny-cell-shape-transform-section"></a><span data-ttu-id="a935b-103">[PinY] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="a935b-103">PinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="a935b-104">親図形の原点を基準としたときの、図形の pin (回転の中心) の*y*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="a935b-104">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of its parent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a935b-105">注釈</span><span class="sxs-lookup"><span data-stu-id="a935b-105">Remarks</span></span>

<span data-ttu-id="a935b-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PinY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a935b-106">To get a reference to the PinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a935b-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="a935b-107">Cell name:</span></span>  <br/> | <span data-ttu-id="a935b-108">PinY</span><span class="sxs-lookup"><span data-stu-id="a935b-108">PinY</span></span>  <br/> |
   
<span data-ttu-id="a935b-109">プログラムから、インデックスによって [PinY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a935b-109">To get a reference to the PinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a935b-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a935b-110">Section index:</span></span>  <br/> |<span data-ttu-id="a935b-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a935b-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a935b-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a935b-112">Row index:</span></span>  <br/> |<span data-ttu-id="a935b-113">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="a935b-113">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="a935b-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a935b-114">Cell index:</span></span>  <br/> |<span data-ttu-id="a935b-115">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="a935b-115">**visXFormPinY**</span></span> <br/> |
   

