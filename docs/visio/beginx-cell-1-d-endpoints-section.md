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
description: 親図形の原点を基準としたときの、1-d 図形の始点の x 座標を表します。
ms.openlocfilehash: 34c1ef1b2500c78791fb4822851eb6d485d77f81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360390"
---
# <a name="beginx-cell-1-d-endpoints-section"></a><span data-ttu-id="87c3d-103">[BeginX] セル ([1-D Endpoints] セクション)</span><span class="sxs-lookup"><span data-stu-id="87c3d-103">BeginX Cell (1-D Endpoints Section)</span></span>

<span data-ttu-id="87c3d-104">親図形の原点を基準としたときの、1-d 図形の始点の*x*座標を表します。</span><span class="sxs-lookup"><span data-stu-id="87c3d-104">Represents the  *x*  -coordinate of the begin point of the 1-D shape, in relation to the origin of its parent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="87c3d-105">解説</span><span class="sxs-lookup"><span data-stu-id="87c3d-105">Remarks</span></span>

<span data-ttu-id="87c3d-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BeginX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="87c3d-106">To get a reference to the BeginX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87c3d-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="87c3d-107">Cell name:</span></span>  <br/> | <span data-ttu-id="87c3d-108">BeginX</span><span class="sxs-lookup"><span data-stu-id="87c3d-108">BeginX</span></span>  <br/> |
   
<span data-ttu-id="87c3d-109">プログラムから、インデックスによって [BeginX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="87c3d-109">To get a reference to the BeginX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87c3d-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="87c3d-110">Section index:</span></span>  <br/> |<span data-ttu-id="87c3d-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="87c3d-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="87c3d-112">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="87c3d-112">Row index:</span></span>  <br/> |<span data-ttu-id="87c3d-113">**visRowXForm1D**</span><span class="sxs-lookup"><span data-stu-id="87c3d-113">**visRowXForm1D**</span></span> <br/> |
| <span data-ttu-id="87c3d-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="87c3d-114">Cell index:</span></span>  <br/> |<span data-ttu-id="87c3d-115">**vis1DBeginX**</span><span class="sxs-lookup"><span data-stu-id="87c3d-115">**vis1DBeginX**</span></span> <br/> |
   

