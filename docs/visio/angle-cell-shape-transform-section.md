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
ms.openlocfilehash: ff052c5b254f9b49a97f5d362a4643e16a27b85d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804768"
---
# <a name="angle-cell-shape-transform-section"></a><span data-ttu-id="2fa66-104">[Angle] セル ([図形変換] セクション)</span><span class="sxs-lookup"><span data-stu-id="2fa66-104">Angle Cell (Shape Transform Section)</span></span>

<span data-ttu-id="2fa66-p102">親図形を基準としたときの、図形の現在の回転角度を表します。1-D 図形の回転角度を決定する既定の数式は =ATAN2(EndY-BeginY,EndX-BeginX) です。</span><span class="sxs-lookup"><span data-stu-id="2fa66-p102">Represents the shape's current angle of rotation in relation to its parent. The default formula for determining the rotation angle of a 1-D shape is: =ATAN2(EndY-BeginY,EndX-BeginX).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2fa66-107">備考</span><span class="sxs-lookup"><span data-stu-id="2fa66-107">Remarks</span></span>

<span data-ttu-id="2fa66-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Angle] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2fa66-108">To get a reference to the Angle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2fa66-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="2fa66-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2fa66-110">Angle</span><span class="sxs-lookup"><span data-stu-id="2fa66-110">Angle</span></span>  <br/> |
   
<span data-ttu-id="2fa66-111">プログラムから、インデックスによって [Angle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2fa66-111">To get a reference to the Angle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2fa66-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2fa66-112">Section index:</span></span>  <br/> |<span data-ttu-id="2fa66-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2fa66-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2fa66-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2fa66-114">Row index:</span></span>  <br/> |<span data-ttu-id="2fa66-115">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="2fa66-115">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="2fa66-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2fa66-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2fa66-117">**visXFormAngle**</span><span class="sxs-lookup"><span data-stu-id="2fa66-117">**visXFormAngle**</span></span> <br/> |
   

