---
title: '[PageBottomMargin] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: 印刷ページの下余白を指定します。
ms.openlocfilehash: f546d89b8761c6c1b7340af69d2b48f16c180767
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438597"
---
# <a name="pagebottommargin-cell-print-properties-section"></a><span data-ttu-id="0b1c6-103">[PageBottomMargin] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="0b1c6-103">PageBottomMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="0b1c6-104">印刷ページの下余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b1c6-104">Specifies the margin at the bottom of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b1c6-105">注釈</span><span class="sxs-lookup"><span data-stu-id="0b1c6-105">Remarks</span></span>

<span data-ttu-id="0b1c6-p101">この値は物理単位を表し、縮尺または図面の単位には影響されません。たとえば、このセルの値が 0.5 インチなら、ページ単位がフィートの場合でも、この余白は 0.5 インチです。単位が明示されていない場合、既定ではこの値にページ単位が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0b1c6-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.5 in., this margin is 0.5 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="0b1c6-109">別の数式または **CellsU** を使用したプログラムから、名前による [PageBottomMargin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0b1c6-109">To get a reference to the PageBottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0b1c6-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="0b1c6-110">Cell name:</span></span>  <br/> | <span data-ttu-id="0b1c6-111">PageBottomMargin</span><span class="sxs-lookup"><span data-stu-id="0b1c6-111">PageBottomMargin</span></span>  <br/> |
   
<span data-ttu-id="0b1c6-112">プログラムから、インデックスによる [PageBottomMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b1c6-112">To get a reference to the PageBottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0b1c6-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0b1c6-113">Section index:</span></span>  <br/> |<span data-ttu-id="0b1c6-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0b1c6-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0b1c6-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0b1c6-115">Row index:</span></span>  <br/> |<span data-ttu-id="0b1c6-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="0b1c6-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="0b1c6-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0b1c6-117">Cell index:</span></span>  <br/> |<span data-ttu-id="0b1c6-118">**visPrintPropertiesBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="0b1c6-118">**visPrintPropertiesBottomMargin**</span></span> <br/> |
   

