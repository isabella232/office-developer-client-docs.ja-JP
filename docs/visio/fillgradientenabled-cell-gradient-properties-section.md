---
title: '[FillGradientEnabled] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: この図形で塗りつぶしのグラデーションを有効にするかどうかを決定します。
ms.openlocfilehash: 20a38d4c45af163bc00364a45dc31269bf97251f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805389"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="802c5-103">[FillGradientEnabled] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="802c5-103">FillGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="802c5-104">この図形で塗りつぶしのグラデーションを有効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="802c5-104">Determines whether a fill gradient is enabled for this shape.</span></span> 
  
|<span data-ttu-id="802c5-105">**値**</span><span class="sxs-lookup"><span data-stu-id="802c5-105">**Value**</span></span>|<span data-ttu-id="802c5-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="802c5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="802c5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="802c5-107">TRUE</span></span>  <br/> |<span data-ttu-id="802c5-108">グラデーションの塗りつぶしは図形に表示されます。</span><span class="sxs-lookup"><span data-stu-id="802c5-108">Gradient fill is displayed on the shape.</span></span>  <br/> |
|<span data-ttu-id="802c5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="802c5-109">FALSE</span></span>  <br/> |<span data-ttu-id="802c5-110">グラデーションの塗りつぶしは図形には表示されません。</span><span class="sxs-lookup"><span data-stu-id="802c5-110">Gradient fills are not displayed on the shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="802c5-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="802c5-111">Remarks</span></span>

<span data-ttu-id="802c5-112">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **FillGradientEnabled** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="802c5-112">To get a reference to the **FillGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="802c5-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="802c5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="802c5-114">FillGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="802c5-114">FillGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="802c5-115">プログラムから、インデックスによって [ **FillGradientEnabled** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="802c5-115">To get a reference to the **FillGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="802c5-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="802c5-116">Section index:</span></span>  <br/> |<span data-ttu-id="802c5-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="802c5-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="802c5-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="802c5-118">Row index:</span></span>  <br/> |<span data-ttu-id="802c5-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="802c5-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="802c5-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="802c5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="802c5-121">* * visFillGradientEnabled * *</span><span class="sxs-lookup"><span data-stu-id="802c5-121">**visFillGradientEnabled **</span></span> <br/> |
   

