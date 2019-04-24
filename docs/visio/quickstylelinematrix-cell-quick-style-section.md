---
title: '[QuickStyleLineMatrix] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b10221d-30f8-48f5-81ed-0283fdfc3e5d
description: 図形が継承するクイックスタイルの線のスタイルを、0-6 からの整数で指定します。
ms.openlocfilehash: e04fc6328d40b0564364aa8feff971628360d813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282587"
---
# <a name="quickstylelinematrix-cell-quick-style-section"></a><span data-ttu-id="2d9d1-103">[QuickStyleLineMatrix] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="2d9d1-103">QuickStyleLineMatrix Cell (Quick Style Section)</span></span>

<span data-ttu-id="2d9d1-104">図形が継承するクイックスタイルの線のスタイルを、0-6 からの整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="2d9d1-104">Determines the Quick Style line style that the shape inherits, as an integer from 0-6.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2d9d1-105">解説</span><span class="sxs-lookup"><span data-stu-id="2d9d1-105">Remarks</span></span>

<span data-ttu-id="2d9d1-106">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[quickstylelinematrix]** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2d9d1-106">To get a reference to the **QuickStyleLineMatrix** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d9d1-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="2d9d1-107">Cell name:</span></span>  <br/> | <span data-ttu-id="2d9d1-108">[quickstylelinematrix]</span><span class="sxs-lookup"><span data-stu-id="2d9d1-108">QuickStyleLineMatrix</span></span>  <br/> |
   
<span data-ttu-id="2d9d1-109">プログラムから、インデックスによって [ **[quickstylelinematrix]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2d9d1-109">To get a reference to the **QuickStyleLineMatrix** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d9d1-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2d9d1-110">Section index:</span></span>  <br/> |<span data-ttu-id="2d9d1-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2d9d1-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2d9d1-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2d9d1-112">Row index:</span></span>  <br/> |<span data-ttu-id="2d9d1-113">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="2d9d1-113">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="2d9d1-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2d9d1-114">Cell index:</span></span>  <br/> |<span data-ttu-id="2d9d1-115">**visQuickStyleLineMatrix**</span><span class="sxs-lookup"><span data-stu-id="2d9d1-115">**visQuickStyleLineMatrix**</span></span> <br/> |
   

