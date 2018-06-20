---
title: '[EndX] セル ([1-D Endpoints] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm335
localization_priority: Normal
ms.assetid: 24261b77-e3e8-7434-a503-9f23798bdab1
description: X を表しますが、親の原点を基準として、1 次元図形の端点の座標です。
ms.openlocfilehash: f7324d9d4df5c428f734da255e7dd65b24cb0cb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805325"
---
# <a name="endx-cell-1-d-endpoints-section"></a><span data-ttu-id="d95c4-103">[EndX] セル ([1-D Endpoints] セクション)</span><span class="sxs-lookup"><span data-stu-id="d95c4-103">EndX Cell (1-D Endpoints Section)</span></span>

<span data-ttu-id="d95c4-104">*X*を表しますが、親の原点を基準として、1 次元図形の端点の座標です。</span><span class="sxs-lookup"><span data-stu-id="d95c4-104">Represents the  *x*  -coordinate of the endpoint of the 1-D shape, in relation to the origin of its parent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d95c4-105">備考</span><span class="sxs-lookup"><span data-stu-id="d95c4-105">Remarks</span></span>

<span data-ttu-id="d95c4-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [endx] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d95c4-106">To get a reference to the EndX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d95c4-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="d95c4-107">Cell name:</span></span>  <br/> | <span data-ttu-id="d95c4-108">[Endx]</span><span class="sxs-lookup"><span data-stu-id="d95c4-108">EndX</span></span>  <br/> |
   
<span data-ttu-id="d95c4-109">プログラムから、インデックスによって [endx] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d95c4-109">To get a reference to the EndX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d95c4-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d95c4-110">Section index:</span></span>  <br/> |<span data-ttu-id="d95c4-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d95c4-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d95c4-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d95c4-112">Row index:</span></span>  <br/> |<span data-ttu-id="d95c4-113">**visRowXForm1D**</span><span class="sxs-lookup"><span data-stu-id="d95c4-113">**visRowXForm1D**</span></span> <br/> |
| <span data-ttu-id="d95c4-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d95c4-114">Cell index:</span></span>  <br/> |<span data-ttu-id="d95c4-115">**vis1DEndX**</span><span class="sxs-lookup"><span data-stu-id="d95c4-115">**vis1DEndX**</span></span> <br/> |
   

