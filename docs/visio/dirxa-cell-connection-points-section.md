---
title: '[DirX / A] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: 一致する接続ポイントに必要な配置ベクトルの x コンポーネントを決定します。 [DirX / A] セルは、動的コネクタに付いている足の向きを揃える場合にも使用されます。 このセルでは浮動小数点値が使用されます。
ms.openlocfilehash: cb86ef1064537911ffd00a66f5c0b7942459f85e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332594"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="c84f6-105">[DirX / A] セル ([Connection Points] セクション)</span><span class="sxs-lookup"><span data-stu-id="c84f6-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="c84f6-106">一致する接続ポイントに必要な配置ベクトルの*x*コンポーネントを決定します。</span><span class="sxs-lookup"><span data-stu-id="c84f6-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="c84f6-107">[DirX / A] セルは、動的コネクタに付いている足の向きを揃える場合にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="c84f6-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="c84f6-108">このセルでは浮動小数点値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c84f6-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c84f6-109">解説</span><span class="sxs-lookup"><span data-stu-id="c84f6-109">Remarks</span></span>

<span data-ttu-id="c84f6-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DirX / A] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c84f6-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c84f6-111">セル名 :</span><span class="sxs-lookup"><span data-stu-id="c84f6-111">Cell name:</span></span>  <br/> | <span data-ttu-id="c84f6-112">[dirx [ *i* ] = <1>、 \*\* 2、3...</span><span class="sxs-lookup"><span data-stu-id="c84f6-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c84f6-113">プログラムから、インデックスによって [DirX / A] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c84f6-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c84f6-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c84f6-114">Section index:</span></span>  <br/> |<span data-ttu-id="c84f6-115">**持つ vissectionconnectionpts**</span><span class="sxs-lookup"><span data-stu-id="c84f6-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="c84f6-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c84f6-116">Row index:</span></span>  <br/> |<span data-ttu-id="c84f6-117">**visRowConnectionPts** +  *i* = \*\* 0、1、2</span><span class="sxs-lookup"><span data-stu-id="c84f6-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="c84f6-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c84f6-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c84f6-119">**visCnnctDirX**(非拡張行)          **visCnnctA**(拡張行)</span><span class="sxs-lookup"><span data-stu-id="c84f6-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="c84f6-120">拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c84f6-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

