---
title: '[TxtWidth] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: テキスト ブロックの幅を指定します。既定の数式は次のとおりです。
ms.openlocfilehash: ecba66aaf1f7eeb6d16c6b0d4c6569aed051910f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806723"
---
# <a name="txtwidth-cell-text-transform-section"></a><span data-ttu-id="e6bcb-104">[TxtWidth] セル ([テキスト変換] セクション)</span><span class="sxs-lookup"><span data-stu-id="e6bcb-104">TxtWidth Cell (Text Transform Section)</span></span>

<span data-ttu-id="e6bcb-p102">テキスト ブロックの幅を指定します。既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e6bcb-p102">Determines the width of the text block. The default formula is:</span></span>
  
<span data-ttu-id="e6bcb-107">= 幅\*1</span><span class="sxs-lookup"><span data-stu-id="e6bcb-107">= Width \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6bcb-108">注釈</span><span class="sxs-lookup"><span data-stu-id="e6bcb-108">Remarks</span></span>

<span data-ttu-id="e6bcb-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtWidth] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e6bcb-109">To get a reference to the TxtWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e6bcb-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="e6bcb-110">Cell name:</span></span>  <br/> | <span data-ttu-id="e6bcb-111">[Txtwidth]</span><span class="sxs-lookup"><span data-stu-id="e6bcb-111">TxtWidth</span></span>  <br/> |
   
<span data-ttu-id="e6bcb-112">プログラムから、インデックスによって [TxtWidth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e6bcb-112">To get a reference to the TxtWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e6bcb-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e6bcb-113">Section index:</span></span>  <br/> |<span data-ttu-id="e6bcb-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e6bcb-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e6bcb-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e6bcb-115">Row index:</span></span>  <br/> |<span data-ttu-id="e6bcb-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="e6bcb-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="e6bcb-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e6bcb-117">Cell index:</span></span>  <br/> |<span data-ttu-id="e6bcb-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="e6bcb-118">**visXFormWidth**</span></span> <br/> |
   

