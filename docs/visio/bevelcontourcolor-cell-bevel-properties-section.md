---
title: '[BevelContourColor] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 90bc9be5-282e-4a84-9d8b-e11788070768
description: ベベルの RGB 値の配分やテーマによって、決められた色を決定します。
ms.openlocfilehash: 89b90f804ce1ccd8511dc0160f1ca2c94546596e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804810"
---
# <a name="bevelcontourcolor-cell-bevel-properties-section"></a><span data-ttu-id="402a0-103">[BevelContourColor] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="402a0-103">BevelContourColor Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="402a0-104">ベベルの RGB 値の配分やテーマによって、決められた色を決定します。</span><span class="sxs-lookup"><span data-stu-id="402a0-104">Determines the color of the bevel's contour in RGB value or as determined by the active theme.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="402a0-105">備考</span><span class="sxs-lookup"><span data-stu-id="402a0-105">Remarks</span></span>

<span data-ttu-id="402a0-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **BevelContourColor** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="402a0-106">To get a reference to the **BevelContourColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="402a0-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="402a0-107">Cell name:</span></span>  <br/> | <span data-ttu-id="402a0-108">BevelContourColor</span><span class="sxs-lookup"><span data-stu-id="402a0-108">BevelContourColor</span></span>  <br/> |
   
<span data-ttu-id="402a0-109">プログラムから、インデックスによって [ **BevelContourColor** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="402a0-109">To get a reference to the **BevelContourColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="402a0-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="402a0-110">Section index:</span></span>  <br/> |<span data-ttu-id="402a0-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="402a0-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="402a0-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="402a0-112">Row index:</span></span>  <br/> |<span data-ttu-id="402a0-113">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="402a0-113">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="402a0-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="402a0-114">Cell index:</span></span>  <br/> |<span data-ttu-id="402a0-115">**vis BevelContourColor**</span><span class="sxs-lookup"><span data-stu-id="402a0-115">**vis BevelContourColor**</span></span> <br/> |
   

