---
title: '[PageTopMargin] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
localization_priority: Normal
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: 印刷ページの上余白を指定します。
ms.openlocfilehash: ff2bffffed39c5571386e792d2ffc8d20d6b291e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416581"
---
# <a name="pagetopmargin-cell-print-properties-section"></a><span data-ttu-id="d7df0-103">[PageTopMargin] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="d7df0-103">PageTopMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="d7df0-104">印刷ページの上余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7df0-104">Specifies the margin at the top of the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7df0-105">注釈</span><span class="sxs-lookup"><span data-stu-id="d7df0-105">Remarks</span></span>

<span data-ttu-id="d7df0-p101">この値は物理単位を表し、縮尺または図面の単位には影響されません。たとえば、このセルの値が 0.25 インチなら、ページ単位がフィートの場合でも、この余白は 0.25 インチです。単位が明示されていない場合、既定ではこの値にページ単位が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d7df0-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="d7df0-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageTopMargin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d7df0-109">To get a reference to the PageTopMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7df0-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="d7df0-110">Cell name:</span></span>  <br/> | <span data-ttu-id="d7df0-111">[pagetopmargin]</span><span class="sxs-lookup"><span data-stu-id="d7df0-111">PageTopMargin</span></span>  <br/> |
   
<span data-ttu-id="d7df0-112">プログラムから、インデックスによって [PageTopMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7df0-112">To get a reference to the PageTopMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7df0-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d7df0-113">Section index:</span></span>  <br/> |<span data-ttu-id="d7df0-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d7df0-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d7df0-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d7df0-115">Row index:</span></span>  <br/> |<span data-ttu-id="d7df0-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="d7df0-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="d7df0-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d7df0-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d7df0-118">**visPrintPropertiesTopMargin**</span><span class="sxs-lookup"><span data-stu-id="d7df0-118">**visPrintPropertiesTopMargin**</span></span> <br/> |
   

