---
title: '[LocPinX] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: X を表す-図形の原点を基準として、図形の pin (回転の中心) の座標。 [Locpinx] を決定するための既定の数式は次のとおりです。
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805802"
---
# <a name="locpinx-cell-shape-transform-section"></a><span data-ttu-id="365a2-104">[LocPinX] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="365a2-104">LocPinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="365a2-105">*X*を表す-図形の原点を基準として、図形の pin (回転の中心) の座標。</span><span class="sxs-lookup"><span data-stu-id="365a2-105">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="365a2-106">[Locpinx] を決定するための既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="365a2-106">The default formula for determining LocPinX is:</span></span> 
  
<span data-ttu-id="365a2-107">= 幅\*0.5</span><span class="sxs-lookup"><span data-stu-id="365a2-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="365a2-108">備考</span><span class="sxs-lookup"><span data-stu-id="365a2-108">Remarks</span></span>

<span data-ttu-id="365a2-109">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [locpinx] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="365a2-109">To get a reference to the LocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="365a2-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="365a2-110">Cell name:</span></span>  <br/> | <span data-ttu-id="365a2-111">[Locpinx]</span><span class="sxs-lookup"><span data-stu-id="365a2-111">LocPinX</span></span>  <br/> |
   
<span data-ttu-id="365a2-112">プログラムから、インデックスによって [locpinx] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="365a2-112">To get a reference to the LocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="365a2-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="365a2-113">Section index:</span></span>  <br/> |<span data-ttu-id="365a2-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="365a2-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="365a2-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="365a2-115">Row index:</span></span>  <br/> |<span data-ttu-id="365a2-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="365a2-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="365a2-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="365a2-117">Cell index:</span></span>  <br/> |<span data-ttu-id="365a2-118">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="365a2-118">**visXFormLocPinX**</span></span> <br/> |
   

