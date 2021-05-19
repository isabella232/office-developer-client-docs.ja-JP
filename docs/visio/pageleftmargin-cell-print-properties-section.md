---
title: '[PageLeftMargin] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: 印刷ページの左余白を指定します。
ms.openlocfilehash: 289bd0bf16c6dcd9b26ec1a8c7920a29dab724a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435671"
---
# <a name="pageleftmargin-cell-print-properties-section"></a><span data-ttu-id="847ed-103">[PageLeftMargin] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="847ed-103">PageLeftMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="847ed-104">印刷ページの左余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="847ed-104">Specifies the margin on the left of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="847ed-105">注釈</span><span class="sxs-lookup"><span data-stu-id="847ed-105">Remarks</span></span>

<span data-ttu-id="847ed-p101">この値は物理単位を表し、縮尺または図面の単位には影響されません。たとえば、このセルの値が 0.25 インチなら、ページ単位がフィートの場合でも、この余白は 0.25 インチです。単位が明示されていない場合、既定ではこの値にページ単位が使用されます。</span><span class="sxs-lookup"><span data-stu-id="847ed-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="847ed-109">別の数式または **CellsU** を使用したプログラムから、名前による [PageLeftMargin] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="847ed-109">To get a reference to the PageLeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="847ed-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="847ed-110">Cell name:</span></span>  <br/> | <span data-ttu-id="847ed-111">PageLeftMargin</span><span class="sxs-lookup"><span data-stu-id="847ed-111">PageLeftMargin</span></span>  <br/> |
   
<span data-ttu-id="847ed-112">プログラムから、インデックスによる [PageLeftMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="847ed-112">To get a reference to the PageLeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="847ed-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="847ed-113">Section index:</span></span>  <br/> |<span data-ttu-id="847ed-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="847ed-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="847ed-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="847ed-115">Row index:</span></span>  <br/> |<span data-ttu-id="847ed-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="847ed-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="847ed-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="847ed-117">Cell index:</span></span>  <br/> |<span data-ttu-id="847ed-118">**visPrintPropertiesLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="847ed-118">**visPrintPropertiesLeftMargin**</span></span> <br/> |
   

