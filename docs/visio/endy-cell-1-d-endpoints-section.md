---
title: '[EndY] セル ([1-D Endpoints] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm340
localization_priority: Normal
ms.assetid: 3fbfa4bc-7792-b6d9-d549-4602d252c293
description: Y を表しますが、親の原点を基準として、1 次元図形の端点の座標です。
ms.openlocfilehash: 4c619a9c7c37ba892931f08b37c3beb0efac7531
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805316"
---
# <a name="endy-cell-1-d-endpoints-section"></a><span data-ttu-id="85c9c-103">[EndY] セル ([1-D Endpoints] セクション)</span><span class="sxs-lookup"><span data-stu-id="85c9c-103">EndY Cell (1-D Endpoints Section)</span></span>

<span data-ttu-id="85c9c-104">*Y*を表すが、親の原点を基準として、1 次元図形の端点の座標です。</span><span class="sxs-lookup"><span data-stu-id="85c9c-104">Represents the  *y*  -coordinate of the endpoint of the 1-D shape, in relation to the origin of its parent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="85c9c-105">備考</span><span class="sxs-lookup"><span data-stu-id="85c9c-105">Remarks</span></span>

<span data-ttu-id="85c9c-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [endy] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="85c9c-106">To get a reference to the EndY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="85c9c-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="85c9c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="85c9c-108">[Endy]</span><span class="sxs-lookup"><span data-stu-id="85c9c-108">EndY</span></span>  <br/> |
   
<span data-ttu-id="85c9c-109">プログラムから、インデックスによって [endy] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="85c9c-109">To get a reference to the EndY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="85c9c-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="85c9c-110">Section index:</span></span>  <br/> |<span data-ttu-id="85c9c-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="85c9c-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="85c9c-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="85c9c-112">Row index:</span></span>  <br/> |<span data-ttu-id="85c9c-113">**visRowXForm1D**</span><span class="sxs-lookup"><span data-stu-id="85c9c-113">**visRowXForm1D**</span></span> <br/> |
| <span data-ttu-id="85c9c-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="85c9c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="85c9c-115">**vis1DEndY**</span><span class="sxs-lookup"><span data-stu-id="85c9c-115">**vis1DEndY**</span></span> <br/> |
   

