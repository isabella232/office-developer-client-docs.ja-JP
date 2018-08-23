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
description: X を決定に対応する接続ポイントの必要な整列ベクトルのコンポーネントです。 DirX/動的コネクタに付いている足の方向を設定するセルを使用しても。 このセルでは浮動小数点値です。
ms.openlocfilehash: 49feba7cefbccc4efcbd04e8940c1f801563539e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805246"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="fd862-105">[DirX / A] セル ([接続ポイント] セクション)</span><span class="sxs-lookup"><span data-stu-id="fd862-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="fd862-106">*X*を決定に対応する接続ポイントの必要な整列ベクトルのコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="fd862-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="fd862-107">DirX/動的コネクタに付いている足の方向を設定するセルを使用しても。</span><span class="sxs-lookup"><span data-stu-id="fd862-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="fd862-108">このセルでは浮動小数点値です。</span><span class="sxs-lookup"><span data-stu-id="fd862-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fd862-109">注釈</span><span class="sxs-lookup"><span data-stu-id="fd862-109">Remarks</span></span>

<span data-ttu-id="fd862-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DirX / A] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fd862-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd862-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="fd862-111">Cell name:</span></span>  <br/> | <span data-ttu-id="fd862-112">Connections.DirX [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="fd862-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fd862-113">プログラムから、インデックスによって [DirX / A] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd862-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd862-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fd862-114">Section index:</span></span>  <br/> |<span data-ttu-id="fd862-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="fd862-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="fd862-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fd862-116">Row index:</span></span>  <br/> |<span data-ttu-id="fd862-117">**visRowConnectionPts** +  *i* 、 *i* = 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="fd862-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="fd862-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fd862-118">Cell index:</span></span>  <br/> |<span data-ttu-id="fd862-119">**visCnnctDirX**(拡張されていない行)          **visCnnctA**(拡張された行)</span><span class="sxs-lookup"><span data-stu-id="fd862-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="fd862-120">拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd862-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

