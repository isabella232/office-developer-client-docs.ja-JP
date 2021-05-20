---
title: '[FillGradientEnabled] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: この図形で塗りつぶしのグラデーションを有効にするかどうかを決定します。
ms.openlocfilehash: 17f617c13b632318be22b86a3354a194f0f835f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431212"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="54c56-103">[FillGradientEnabled] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="54c56-103">FillGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="54c56-104">この図形で塗りつぶしのグラデーションを有効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="54c56-104">Determines whether a fill gradient is enabled for this shape.</span></span> 
  
|<span data-ttu-id="54c56-105">**値**</span><span class="sxs-lookup"><span data-stu-id="54c56-105">**Value**</span></span>|<span data-ttu-id="54c56-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="54c56-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="54c56-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="54c56-107">TRUE</span></span>  <br/> |<span data-ttu-id="54c56-108">グラデーションの塗りつぶしは図形に表示されます。</span><span class="sxs-lookup"><span data-stu-id="54c56-108">Gradient fill is displayed on the shape.</span></span>  <br/> |
|<span data-ttu-id="54c56-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="54c56-109">FALSE</span></span>  <br/> |<span data-ttu-id="54c56-110">グラデーションの塗りつぶしは図形には表示されません。</span><span class="sxs-lookup"><span data-stu-id="54c56-110">Gradient fills are not displayed on the shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54c56-111">注釈</span><span class="sxs-lookup"><span data-stu-id="54c56-111">Remarks</span></span>

<span data-ttu-id="54c56-112">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**FillGradientEnabled**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="54c56-112">To get a reference to the **FillGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54c56-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="54c56-113">Cell name:</span></span>  <br/> | <span data-ttu-id="54c56-114">FillGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="54c56-114">FillGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="54c56-115">プログラムから、インデックスによって [**FillGradientEnabled**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="54c56-115">To get a reference to the **FillGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54c56-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="54c56-116">Section index:</span></span>  <br/> |<span data-ttu-id="54c56-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="54c56-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="54c56-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="54c56-118">Row index:</span></span>  <br/> |<span data-ttu-id="54c56-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="54c56-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="54c56-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="54c56-120">Cell index:</span></span>  <br/> |<span data-ttu-id="54c56-121">\*\*visFillGradientEnabled \*\*</span><span class="sxs-lookup"><span data-stu-id="54c56-121">\*\*visFillGradientEnabled \*\*</span></span> <br/> |
   

