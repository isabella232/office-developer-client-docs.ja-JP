---
title: '[FlipY] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
localization_priority: Normal
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: 図形が上下反転されているかを示します。
ms.openlocfilehash: 44ea0341cda3655e8acc69e82e89acddac69b80d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417449"
---
# <a name="flipy-cell-shape-transform-section"></a><span data-ttu-id="3577b-103">[FlipY] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="3577b-103">FlipY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="3577b-104">図形が上下反転されているかを示します。</span><span class="sxs-lookup"><span data-stu-id="3577b-104">Indicates whether the shape has been flipped vertically.</span></span>
  
|<span data-ttu-id="3577b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="3577b-105">**Value**</span></span>|<span data-ttu-id="3577b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="3577b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3577b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3577b-107">TRUE</span></span>  <br/> | <span data-ttu-id="3577b-108">図形は上下反転されています。</span><span class="sxs-lookup"><span data-stu-id="3577b-108">The shape has been flipped vertically.</span></span>  <br/> |
| <span data-ttu-id="3577b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3577b-109">FALSE</span></span>  <br/> | <span data-ttu-id="3577b-110">図形は上下反転されていません。</span><span class="sxs-lookup"><span data-stu-id="3577b-110">The shape has not been flipped vertically.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3577b-111">注釈</span><span class="sxs-lookup"><span data-stu-id="3577b-111">Remarks</span></span>

<span data-ttu-id="3577b-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FlipY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3577b-112">To get a reference to the FlipY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3577b-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="3577b-113">Cell name:</span></span>  <br/> | <span data-ttu-id="3577b-114">FlipY</span><span class="sxs-lookup"><span data-stu-id="3577b-114">FlipY</span></span>  <br/> |
   
<span data-ttu-id="3577b-115">プログラムから、インデックスによって [FlipY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3577b-115">To get a reference to the FlipY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3577b-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3577b-116">Section index:</span></span>  <br/> |<span data-ttu-id="3577b-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3577b-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3577b-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3577b-118">Row index:</span></span>  <br/> |<span data-ttu-id="3577b-119">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="3577b-119">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="3577b-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3577b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="3577b-121">**visXFormFlipY**</span><span class="sxs-lookup"><span data-stu-id="3577b-121">**visXFormFlipY**</span></span> <br/> |
   

