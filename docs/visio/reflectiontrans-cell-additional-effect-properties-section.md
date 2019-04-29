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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425681"
---
# <a name="reflectiontrans-cell-additional-effect-properties-section"></a><span data-ttu-id="4d6e1-103">[ReflectionTrans] セル ([追加効果のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="4d6e1-103">ReflectionTrans Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="4d6e1-104">反射の透明度を 0 ~ 100% の割合で指定します。</span><span class="sxs-lookup"><span data-stu-id="4d6e1-104">Determines the transparency of the reflection, as a percentage from 0 to 100%.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4d6e1-105">注釈</span><span class="sxs-lookup"><span data-stu-id="4d6e1-105">Remarks</span></span>

<span data-ttu-id="4d6e1-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[reflectiontrans]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4d6e1-106">To get a reference to the **ReflectionTrans** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d6e1-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="4d6e1-107">Cell name:</span></span>  <br/> | <span data-ttu-id="4d6e1-108">[reflectiontrans]</span><span class="sxs-lookup"><span data-stu-id="4d6e1-108">ReflectionTrans</span></span>  <br/> |
   
<span data-ttu-id="4d6e1-109">プログラムから、インデックスによって [ **[reflectiontrans]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4d6e1-109">To get a reference to the **ReflectionTrans** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d6e1-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4d6e1-110">Section index:</span></span>  <br/> |<span data-ttu-id="4d6e1-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4d6e1-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4d6e1-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4d6e1-112">Row index:</span></span>  <br/> |<span data-ttu-id="4d6e1-113">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="4d6e1-113">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="4d6e1-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4d6e1-114">Cell index:</span></span>  <br/> |<span data-ttu-id="4d6e1-115">**visReflectionTrans**</span><span class="sxs-lookup"><span data-stu-id="4d6e1-115">**visReflectionTrans**</span></span> <br/> |
   

