---
title: '[LineGradientEnabled] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: 線または図形の境界線で線のグラデーションを有効にするかどうかを決定します。
ms.openlocfilehash: d78a94a25c0290bd5e58522c9a45955868f31b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805693"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="53e12-103">[LineGradientEnabled] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="53e12-103">LineGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="53e12-104">線または図形の境界線で線のグラデーションを有効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="53e12-104">Determines whether a line gradient is enabled for a line or border of a shape.</span></span> 
  
|<span data-ttu-id="53e12-105">**値**</span><span class="sxs-lookup"><span data-stu-id="53e12-105">**Value**</span></span>|<span data-ttu-id="53e12-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="53e12-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53e12-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="53e12-107">TRUE</span></span>  <br/> |<span data-ttu-id="53e12-108">グラデーションは、図形の線または境界線に表示されます。</span><span class="sxs-lookup"><span data-stu-id="53e12-108">Gradient is displayed on the line or border of a shape.</span></span>  <br/> |
|<span data-ttu-id="53e12-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="53e12-109">FALSE</span></span>  <br/> |<span data-ttu-id="53e12-110">グラデーションは、図形の線または境界線に表示されません。</span><span class="sxs-lookup"><span data-stu-id="53e12-110">Gradients are not displayed on the line or border of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53e12-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="53e12-111">Remarks</span></span>

<span data-ttu-id="53e12-112">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **LineGradientEnabled** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="53e12-112">To get a reference to the **LineGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="53e12-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="53e12-113">Cell name:</span></span>  <br/> | <span data-ttu-id="53e12-114">LineGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="53e12-114">LineGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="53e12-115">プログラムから、インデックスによって [ **LineGradientEnabled** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="53e12-115">To get a reference to the **LineGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="53e12-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="53e12-116">Section index:</span></span>  <br/> |<span data-ttu-id="53e12-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="53e12-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="53e12-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="53e12-118">Row index:</span></span>  <br/> |<span data-ttu-id="53e12-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="53e12-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="53e12-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="53e12-120">Cell index:</span></span>  <br/> |<span data-ttu-id="53e12-121">**visLineGradientEnabled**</span><span class="sxs-lookup"><span data-stu-id="53e12-121">**visLineGradientEnabled**</span></span> <br/> |
   

