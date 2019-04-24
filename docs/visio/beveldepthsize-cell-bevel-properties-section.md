---
title: '[BevelDepthSize] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c6a57e52-c7ed-4a52-940f-1cef9baa70a5
description: 面取りの奥行きのサイズをポイント単位で指定します。
ms.openlocfilehash: 13c00536d6fc4f19ff2c62cab2afd04f9cdf8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315779"
---
# <a name="beveldepthsize-cell-bevel-properties-section"></a><span data-ttu-id="0c698-103">[BevelDepthSize] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="0c698-103">BevelDepthSize Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="0c698-104">面取りの奥行きのサイズをポイント単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="0c698-104">Determines the size of the bevel's depth in points.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0c698-105">解説</span><span class="sxs-lookup"><span data-stu-id="0c698-105">Remarks</span></span>

<span data-ttu-id="0c698-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[beveldepthsize]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0c698-106">To get a reference to the **BevelDepthSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0c698-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="0c698-107">Cell name:</span></span>  <br/> | <span data-ttu-id="0c698-108">[beveldepthsize]</span><span class="sxs-lookup"><span data-stu-id="0c698-108">BevelDepthSize</span></span>  <br/> |
   
<span data-ttu-id="0c698-109">プログラムから、インデックスによって [ **[beveldepthsize]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c698-109">To get a reference to the **BevelDepthSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0c698-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0c698-110">Section index:</span></span>  <br/> |<span data-ttu-id="0c698-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0c698-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0c698-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0c698-112">Row index:</span></span>  <br/> |<span data-ttu-id="0c698-113">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="0c698-113">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="0c698-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0c698-114">Cell index:</span></span>  <br/> |<span data-ttu-id="0c698-115">**visBevelDepthSize**</span><span class="sxs-lookup"><span data-stu-id="0c698-115">**visBevelDepthSize**</span></span> <br/> |
   

