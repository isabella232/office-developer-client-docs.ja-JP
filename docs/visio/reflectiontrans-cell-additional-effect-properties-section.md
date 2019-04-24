---
title: '[ReflectionTrans] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1d155af5-b809-4367-b093-1218a1597656
description: 反射の透明度を 0 ~ 100% の割合で指定します。
ms.openlocfilehash: c8d4d83882a1e8eafcd93506f8f8b386828a89cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346488"
---
# <a name="reflectiontrans-cell-additional-effect-properties-section"></a><span data-ttu-id="87d3b-103">[ReflectionTrans] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="87d3b-103">ReflectionTrans Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="87d3b-104">反射の透明度を 0 ~ 100% の割合で指定します。</span><span class="sxs-lookup"><span data-stu-id="87d3b-104">Determines the transparency of the reflection, as a percentage from 0 to 100%.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="87d3b-105">解説</span><span class="sxs-lookup"><span data-stu-id="87d3b-105">Remarks</span></span>

<span data-ttu-id="87d3b-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[reflectiontrans]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="87d3b-106">To get a reference to the **ReflectionTrans** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87d3b-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="87d3b-107">Cell name:</span></span>  <br/> | <span data-ttu-id="87d3b-108">[reflectiontrans]</span><span class="sxs-lookup"><span data-stu-id="87d3b-108">ReflectionTrans</span></span>  <br/> |
   
<span data-ttu-id="87d3b-109">プログラムから、インデックスによって [ **[reflectiontrans]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="87d3b-109">To get a reference to the **ReflectionTrans** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87d3b-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="87d3b-110">Section index:</span></span>  <br/> |<span data-ttu-id="87d3b-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="87d3b-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="87d3b-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="87d3b-112">Row index:</span></span>  <br/> |<span data-ttu-id="87d3b-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="87d3b-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="87d3b-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="87d3b-114">Cell index:</span></span>  <br/> |<span data-ttu-id="87d3b-115">**visReflectionTrans**</span><span class="sxs-lookup"><span data-stu-id="87d3b-115">**visReflectionTrans**</span></span> <br/> |
   

