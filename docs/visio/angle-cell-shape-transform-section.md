---
title: '[Angle] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: 親図形を基準としたときの、図形の現在の回転角度を表します。1-D 図形の回転角度を決定する既定の数式は =ATAN2(EndY-BeginY,EndX-BeginX) です。
ms.openlocfilehash: 85f64c6111b492940d278a5558508a2dea6b1e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341469"
---
# <a name="angle-cell-shape-transform-section"></a><span data-ttu-id="ebabd-104">[Angle] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="ebabd-104">Angle Cell (Shape Transform Section)</span></span>

<span data-ttu-id="ebabd-p102">親図形を基準としたときの、図形の現在の回転角度を表します。1-D 図形の回転角度を決定する既定の数式は =ATAN2(EndY-BeginY,EndX-BeginX) です。</span><span class="sxs-lookup"><span data-stu-id="ebabd-p102">Represents the shape's current angle of rotation in relation to its parent. The default formula for determining the rotation angle of a 1-D shape is: =ATAN2(EndY-BeginY,EndX-BeginX).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ebabd-107">解説</span><span class="sxs-lookup"><span data-stu-id="ebabd-107">Remarks</span></span>

<span data-ttu-id="ebabd-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Angle] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ebabd-108">To get a reference to the Angle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ebabd-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="ebabd-109">Cell name:</span></span>  <br/> | <span data-ttu-id="ebabd-110">角度</span><span class="sxs-lookup"><span data-stu-id="ebabd-110">Angle</span></span>  <br/> |
   
<span data-ttu-id="ebabd-111">プログラムから、インデックスによって [Angle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ebabd-111">To get a reference to the Angle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ebabd-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ebabd-112">Section index:</span></span>  <br/> |<span data-ttu-id="ebabd-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ebabd-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ebabd-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ebabd-114">Row index:</span></span>  <br/> |<span data-ttu-id="ebabd-115">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="ebabd-115">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="ebabd-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ebabd-116">Cell index:</span></span>  <br/> |<span data-ttu-id="ebabd-117">**visXFormAngle**</span><span class="sxs-lookup"><span data-stu-id="ebabd-117">**visXFormAngle**</span></span> <br/> |
   

