---
title: '[TxtHeight] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: テキスト ブロックの高さを指定します。既定の数式は次のとおりです。
ms.openlocfilehash: 8ad17cdf1deca6c4aa81f3388d7c112b4e179e2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409308"
---
# <a name="txtheight-cell-text-transform-section"></a><span data-ttu-id="05a1a-104">[TxtHeight] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="05a1a-104">TxtHeight Cell (Text Transform Section)</span></span>

<span data-ttu-id="05a1a-p102">テキスト ブロックの高さを指定します。既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="05a1a-p102">Determines the height of the text block. The default formula is:</span></span>
  
<span data-ttu-id="05a1a-107">= 高 \* さ 1</span><span class="sxs-lookup"><span data-stu-id="05a1a-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05a1a-108">注釈</span><span class="sxs-lookup"><span data-stu-id="05a1a-108">Remarks</span></span>

<span data-ttu-id="05a1a-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtHeight] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="05a1a-109">To get a reference to the TxtHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05a1a-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="05a1a-110">Cell name:</span></span>  <br/> | <span data-ttu-id="05a1a-111">TxtHeight</span><span class="sxs-lookup"><span data-stu-id="05a1a-111">TxtHeight</span></span>  <br/> |
   
<span data-ttu-id="05a1a-112">プログラムから、インデックスによって [TxtHeight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="05a1a-112">To get a reference to the TxtHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05a1a-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="05a1a-113">Section index:</span></span>  <br/> |<span data-ttu-id="05a1a-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="05a1a-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="05a1a-115">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="05a1a-115">Row index:</span></span>  <br/> |<span data-ttu-id="05a1a-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="05a1a-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="05a1a-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="05a1a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="05a1a-118">**visXFormHeight**</span><span class="sxs-lookup"><span data-stu-id="05a1a-118">**visXFormHeight**</span></span> <br/> |
   

