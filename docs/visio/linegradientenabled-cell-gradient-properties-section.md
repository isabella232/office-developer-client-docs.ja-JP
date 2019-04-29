---
title: '[LineGradientEnabled] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: 線または図形の境界線で線のグラデーションを有効にするかどうかを決定します。
ms.openlocfilehash: 1d2b33275d26bb0c8e5550bcb7cf282c64d34544
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416378"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="a99ad-103">[LineGradientEnabled] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="a99ad-103">LineGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="a99ad-104">線または図形の境界線で線のグラデーションを有効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a99ad-104">Determines whether a line gradient is enabled for a line or border of a shape.</span></span> 
  
|<span data-ttu-id="a99ad-105">**値**</span><span class="sxs-lookup"><span data-stu-id="a99ad-105">**Value**</span></span>|<span data-ttu-id="a99ad-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="a99ad-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a99ad-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a99ad-107">TRUE</span></span>  <br/> |<span data-ttu-id="a99ad-108">グラデーションは、図形の線または境界線に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a99ad-108">Gradient is displayed on the line or border of a shape.</span></span>  <br/> |
|<span data-ttu-id="a99ad-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a99ad-109">FALSE</span></span>  <br/> |<span data-ttu-id="a99ad-110">グラデーションは、図形の線または境界線に表示されません。</span><span class="sxs-lookup"><span data-stu-id="a99ad-110">Gradients are not displayed on the line or border of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a99ad-111">注釈</span><span class="sxs-lookup"><span data-stu-id="a99ad-111">Remarks</span></span>

<span data-ttu-id="a99ad-112">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LineGradientEnabled**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a99ad-112">To get a reference to the **LineGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a99ad-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="a99ad-113">Cell name:</span></span>  <br/> | <span data-ttu-id="a99ad-114">[linegradientenabled]</span><span class="sxs-lookup"><span data-stu-id="a99ad-114">LineGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="a99ad-115">プログラムから、インデックスによって [**LineGradientEnabled**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a99ad-115">To get a reference to the **LineGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a99ad-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a99ad-116">Section index:</span></span>  <br/> |<span data-ttu-id="a99ad-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a99ad-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a99ad-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a99ad-118">Row index:</span></span>  <br/> |<span data-ttu-id="a99ad-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="a99ad-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="a99ad-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a99ad-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a99ad-121">**visLineGradientEnabled**</span><span class="sxs-lookup"><span data-stu-id="a99ad-121">**visLineGradientEnabled**</span></span> <br/> |
   

