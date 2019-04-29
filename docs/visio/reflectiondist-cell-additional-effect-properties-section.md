---
title: '[ReflectionDist] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 858a3191-420a-4065-9180-ebd8503d1eef
description: 反射を図形からオフセットする距離を 0.0 ~ 100.0 の範囲で指定します。
ms.openlocfilehash: cc0aca484a77602b78523819cd4f01d78a9ff86f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433025"
---
# <a name="reflectiondist-cell-additional-effect-properties-section"></a><span data-ttu-id="d40d8-103">[ReflectionDist] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="d40d8-103">ReflectionDist Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="d40d8-104">反射を図形からオフセットする距離を 0.0 ~ 100.0 の範囲で指定します。</span><span class="sxs-lookup"><span data-stu-id="d40d8-104">Determines the distance that a reflection is offset from a shape, in points from 0.0 to 100.0.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d40d8-105">注釈</span><span class="sxs-lookup"><span data-stu-id="d40d8-105">Remarks</span></span>

<span data-ttu-id="d40d8-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[reflectiondist]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d40d8-106">To get a reference to the **ReflectionDist** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d40d8-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="d40d8-107">Cell name:</span></span>  <br/> | <span data-ttu-id="d40d8-108">[reflectiondist]</span><span class="sxs-lookup"><span data-stu-id="d40d8-108">ReflectionDist</span></span>  <br/> |
   
<span data-ttu-id="d40d8-109">プログラムから、インデックスによって [ **[reflectiondist]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d40d8-109">To get a reference to the **ReflectionDist** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d40d8-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d40d8-110">Section index:</span></span>  <br/> |<span data-ttu-id="d40d8-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d40d8-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d40d8-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d40d8-112">Row index:</span></span>  <br/> |<span data-ttu-id="d40d8-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="d40d8-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="d40d8-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d40d8-114">Cell index:</span></span>  <br/> |<span data-ttu-id="d40d8-115">**visReflectionDist**</span><span class="sxs-lookup"><span data-stu-id="d40d8-115">**visReflectionDist**</span></span> <br/> |
   

