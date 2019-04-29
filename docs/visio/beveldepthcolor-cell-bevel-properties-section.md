---
title: '[BevelDepthColor] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1665774f-4049-4eda-ba7a-62314286699e
description: ベベルの奥行きの色を RGB 値で指定します。または、アクティブなテーマによって決定されます。
ms.openlocfilehash: 027b7b8675666b82d0ae26259fe77470708628c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419171"
---
# <a name="beveldepthcolor-cell-bevel-properties-section"></a><span data-ttu-id="06759-103">[BevelDepthColor] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="06759-103">BevelDepthColor Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="06759-104">ベベルの奥行きの色を RGB 値で指定します。または、アクティブなテーマによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="06759-104">Determines the color of the bevel's depth, as an RGB value or as determined by the active theme.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06759-105">注釈</span><span class="sxs-lookup"><span data-stu-id="06759-105">Remarks</span></span>

<span data-ttu-id="06759-106">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**BevelDepthColor**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="06759-106">To get a reference to the **BevelDepthColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="06759-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="06759-107">Cell name:</span></span>  <br/> | <span data-ttu-id="06759-108">[beveldepthcolor]</span><span class="sxs-lookup"><span data-stu-id="06759-108">BevelDepthColor</span></span>  <br/> |
   
<span data-ttu-id="06759-109">プログラムから、インデックスによって [**BevelDepthColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="06759-109">To get a reference to the **BevelDepthColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="06759-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="06759-110">Section index:</span></span>  <br/> |<span data-ttu-id="06759-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="06759-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="06759-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="06759-112">Row index:</span></span>  <br/> |<span data-ttu-id="06759-113">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="06759-113">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="06759-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="06759-114">Cell index:</span></span>  <br/> |<span data-ttu-id="06759-115">**visBevelDepthColor**</span><span class="sxs-lookup"><span data-stu-id="06759-115">**visBevelDepthColor**</span></span> <br/> |
   

