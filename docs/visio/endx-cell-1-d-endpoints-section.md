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
description: 親図形の原点との関係で、1-D 図形の端点の x 座標を表します。
ms.openlocfilehash: 4bd3099b2c13572023b0b813b1cc69a7b211546b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411569"
---
# <a name="endx-cell-1-d-endpoints-section"></a><span data-ttu-id="29319-103">[EndX] セル ([1-D Endpoints] セクション)</span><span class="sxs-lookup"><span data-stu-id="29319-103">EndX Cell (1-D Endpoints Section)</span></span>

<span data-ttu-id="29319-104">親図形  *の原点*  との関係で、1-D 図形の端点の x 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="29319-104">Represents the  *x*  -coordinate of the endpoint of the 1-D shape, in relation to the origin of its parent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="29319-105">注釈</span><span class="sxs-lookup"><span data-stu-id="29319-105">Remarks</span></span>

<span data-ttu-id="29319-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EndX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="29319-106">To get a reference to the EndX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="29319-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="29319-107">Cell name:</span></span>  <br/> | <span data-ttu-id="29319-108">EndX</span><span class="sxs-lookup"><span data-stu-id="29319-108">EndX</span></span>  <br/> |
   
<span data-ttu-id="29319-109">プログラムから、インデックスによって [EndX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="29319-109">To get a reference to the EndX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="29319-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="29319-110">Section index:</span></span>  <br/> |<span data-ttu-id="29319-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="29319-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="29319-112">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="29319-112">Row index:</span></span>  <br/> |<span data-ttu-id="29319-113">**visRowXForm1D**</span><span class="sxs-lookup"><span data-stu-id="29319-113">**visRowXForm1D**</span></span> <br/> |
| <span data-ttu-id="29319-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="29319-114">Cell index:</span></span>  <br/> |<span data-ttu-id="29319-115">**vis1DEndX**</span><span class="sxs-lookup"><span data-stu-id="29319-115">**vis1DEndX**</span></span> <br/> |
   

