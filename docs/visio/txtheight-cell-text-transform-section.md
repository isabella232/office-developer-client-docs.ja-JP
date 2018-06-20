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
ms.openlocfilehash: e9495eef837a61fa9b7ecb2b242fdabc5df30080
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806703"
---
# <a name="txtheight-cell-text-transform-section"></a><span data-ttu-id="fb41d-104">[TxtHeight] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="fb41d-104">TxtHeight Cell (Text Transform Section)</span></span>

<span data-ttu-id="fb41d-p102">テキスト ブロックの高さを指定します。既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fb41d-p102">Determines the height of the text block. The default formula is:</span></span>
  
<span data-ttu-id="fb41d-107">= 高さ\*1</span><span class="sxs-lookup"><span data-stu-id="fb41d-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb41d-108">備考</span><span class="sxs-lookup"><span data-stu-id="fb41d-108">Remarks</span></span>

<span data-ttu-id="fb41d-109">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [txtheight] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="fb41d-109">To get a reference to the TxtHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb41d-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="fb41d-110">Cell name:</span></span>  <br/> | <span data-ttu-id="fb41d-111">[Txtheight]</span><span class="sxs-lookup"><span data-stu-id="fb41d-111">TxtHeight</span></span>  <br/> |
   
<span data-ttu-id="fb41d-112">プログラムから、インデックスによって [txtheight] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb41d-112">To get a reference to the TxtHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb41d-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fb41d-113">Section index:</span></span>  <br/> |<span data-ttu-id="fb41d-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fb41d-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fb41d-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fb41d-115">Row index:</span></span>  <br/> |<span data-ttu-id="fb41d-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="fb41d-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="fb41d-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fb41d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="fb41d-118">**visXFormHeight**</span><span class="sxs-lookup"><span data-stu-id="fb41d-118">**visXFormHeight**</span></span> <br/> |
   

