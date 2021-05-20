---
title: '[NonPrinting] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: 選択した図形の印刷のオン/オフを切り替えます。
ms.openlocfilehash: c3e1fc1b2d91fa4808f8ea89c904218c2236f5b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437260"
---
# <a name="nonprinting-cell-miscellaneous-section"></a><span data-ttu-id="2dce3-103">[NonPrinting] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="2dce3-103">NonPrinting Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="2dce3-104">選択した図形の印刷のオン/オフを切り替えます。</span><span class="sxs-lookup"><span data-stu-id="2dce3-104">Switches printing on and off for the selected shape.</span></span>
  
|<span data-ttu-id="2dce3-105">**値**</span><span class="sxs-lookup"><span data-stu-id="2dce3-105">**Value**</span></span>|<span data-ttu-id="2dce3-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="2dce3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2dce3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2dce3-107">TRUE</span></span>  <br/> | <span data-ttu-id="2dce3-108">印刷は無効になりますが、図形は図面ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2dce3-108">Printing disabled, but the shape will be displayed in the drawing window.</span></span>  <br/> |
| <span data-ttu-id="2dce3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2dce3-109">FALSE</span></span>  <br/> | <span data-ttu-id="2dce3-110">印刷は有効になります。</span><span class="sxs-lookup"><span data-stu-id="2dce3-110">Printing enabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2dce3-111">注釈</span><span class="sxs-lookup"><span data-stu-id="2dce3-111">Remarks</span></span>

<span data-ttu-id="2dce3-112">ガイドを選択し、その [NonPrinting] セルの値を FALSE に設定すると、ガイドを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="2dce3-112">You can print a guide by selecting it, and then setting the value of its NonPrinting cell to FALSE.</span></span>
  
<span data-ttu-id="2dce3-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NonPrinting] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2dce3-113">To get a reference to the NonPrinting cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2dce3-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="2dce3-114">Cell name:</span></span>  <br/> | <span data-ttu-id="2dce3-115">NonPrinting</span><span class="sxs-lookup"><span data-stu-id="2dce3-115">NonPrinting</span></span>  <br/> |
   
<span data-ttu-id="2dce3-116">プログラムから、インデックスによって [NonPrinting] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2dce3-116">To get a reference to the NonPrinting cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2dce3-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2dce3-117">Section index:</span></span>  <br/> |<span data-ttu-id="2dce3-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2dce3-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2dce3-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2dce3-119">Row index:</span></span>  <br/> |<span data-ttu-id="2dce3-120">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="2dce3-120">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="2dce3-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2dce3-121">Cell index:</span></span>  <br/> |<span data-ttu-id="2dce3-122">**visNonPrinting**</span><span class="sxs-lookup"><span data-stu-id="2dce3-122">**visNonPrinting**</span></span> <br/> |
   

