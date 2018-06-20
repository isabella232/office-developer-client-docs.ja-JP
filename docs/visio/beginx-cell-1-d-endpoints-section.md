---
title: '[BeginX] セル ([1-D Endpoints] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm90
localization_priority: Normal
ms.assetid: 59d92820-3ff6-a73d-ffb7-d33096e904f7
description: X を表しますが、親の原点を基準として、1 次元図形の始点の座標です。
ms.openlocfilehash: 2bb68003dddabbde0a77831b19469dedb3ee48b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804816"
---
# <a name="beginx-cell-1-d-endpoints-section"></a><span data-ttu-id="9ca3e-103">[BeginX] セル ([1-D Endpoints] セクション)</span><span class="sxs-lookup"><span data-stu-id="9ca3e-103">BeginX Cell (1-D Endpoints Section)</span></span>

<span data-ttu-id="9ca3e-104">*X*を表しますが、親の原点を基準として、1 次元図形の始点の座標です。</span><span class="sxs-lookup"><span data-stu-id="9ca3e-104">Represents the  *x*  -coordinate of the begin point of the 1-D shape, in relation to the origin of its parent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9ca3e-105">備考</span><span class="sxs-lookup"><span data-stu-id="9ca3e-105">Remarks</span></span>

<span data-ttu-id="9ca3e-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [beginx] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="9ca3e-106">To get a reference to the BeginX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9ca3e-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="9ca3e-107">Cell name:</span></span>  <br/> | <span data-ttu-id="9ca3e-108">[Beginx]</span><span class="sxs-lookup"><span data-stu-id="9ca3e-108">BeginX</span></span>  <br/> |
   
<span data-ttu-id="9ca3e-109">プログラムから、インデックスによって [beginx] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9ca3e-109">To get a reference to the BeginX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9ca3e-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9ca3e-110">Section index:</span></span>  <br/> |<span data-ttu-id="9ca3e-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9ca3e-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9ca3e-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9ca3e-112">Row index:</span></span>  <br/> |<span data-ttu-id="9ca3e-113">**visRowXForm1D**</span><span class="sxs-lookup"><span data-stu-id="9ca3e-113">**visRowXForm1D**</span></span> <br/> |
| <span data-ttu-id="9ca3e-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9ca3e-114">Cell index:</span></span>  <br/> |<span data-ttu-id="9ca3e-115">**vis1DBeginX**</span><span class="sxs-lookup"><span data-stu-id="9ca3e-115">**vis1DBeginX**</span></span> <br/> |
   

