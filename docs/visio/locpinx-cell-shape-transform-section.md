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
description: 図形の原点を基準としたときの、図形の pin (回転の中心) の x 座標を表します。 [LocPinX] を決定する既定の数式は次のとおりです。
ms.openlocfilehash: 2eb5c328eed3c97652173670c426b83b8c358833
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358052"
---
# <a name="locpinx-cell-shape-transform-section"></a><span data-ttu-id="e7869-104">[LocPinX] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="e7869-104">LocPinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="e7869-105">図形の原点を基準としたときの、図形の pin (回転の中心) の*x*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="e7869-105">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="e7869-106">[LocPinX] を決定する既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e7869-106">The default formula for determining LocPinX is:</span></span> 
  
<span data-ttu-id="e7869-107">= 幅\* 0.5</span><span class="sxs-lookup"><span data-stu-id="e7869-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7869-108">解説</span><span class="sxs-lookup"><span data-stu-id="e7869-108">Remarks</span></span>

<span data-ttu-id="e7869-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LocPinX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e7869-109">To get a reference to the LocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e7869-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="e7869-110">Cell name:</span></span>  <br/> | <span data-ttu-id="e7869-111">[locpinx]</span><span class="sxs-lookup"><span data-stu-id="e7869-111">LocPinX</span></span>  <br/> |
   
<span data-ttu-id="e7869-112">プログラムから、インデックスによって [LocPinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7869-112">To get a reference to the LocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e7869-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e7869-113">Section index:</span></span>  <br/> |<span data-ttu-id="e7869-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e7869-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e7869-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e7869-115">Row index:</span></span>  <br/> |<span data-ttu-id="e7869-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="e7869-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="e7869-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e7869-117">Cell index:</span></span>  <br/> |<span data-ttu-id="e7869-118">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="e7869-118">**visXFormLocPinX**</span></span> <br/> |
   

