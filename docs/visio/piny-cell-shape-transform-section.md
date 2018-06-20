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
description: Y を表しますが、親の原点を基準として、図形の pin (回転の中心) の座標。
ms.openlocfilehash: 7002415e813ae63dafb64f416079da2e6b170494
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805990"
---
# <a name="piny-cell-shape-transform-section"></a><span data-ttu-id="d2cf6-103">[PinY] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="d2cf6-103">PinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="d2cf6-104">*Y*を表すが、親の原点を基準として、図形の pin (回転の中心) の座標。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-104">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of its parent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d2cf6-105">備考</span><span class="sxs-lookup"><span data-stu-id="d2cf6-105">Remarks</span></span>

<span data-ttu-id="d2cf6-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [piny] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-106">To get a reference to the PinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2cf6-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="d2cf6-107">Cell name:</span></span>  <br/> | <span data-ttu-id="d2cf6-108">[Piny]</span><span class="sxs-lookup"><span data-stu-id="d2cf6-108">PinY</span></span>  <br/> |
   
<span data-ttu-id="d2cf6-109">プログラムから、インデックスによって [piny] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-109">To get a reference to the PinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2cf6-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d2cf6-110">Section index:</span></span>  <br/> |<span data-ttu-id="d2cf6-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d2cf6-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d2cf6-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d2cf6-112">Row index:</span></span>  <br/> |<span data-ttu-id="d2cf6-113">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="d2cf6-113">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="d2cf6-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d2cf6-114">Cell index:</span></span>  <br/> |<span data-ttu-id="d2cf6-115">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="d2cf6-115">**visXFormPinY**</span></span> <br/> |
   

