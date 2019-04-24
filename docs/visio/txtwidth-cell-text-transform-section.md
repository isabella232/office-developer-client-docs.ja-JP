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
description: テキスト ブロックの幅を指定します。 既定の数式は次のとおりです。
ms.openlocfilehash: 806307166035ebc2f8e20e7025d5ecb03c4d6e79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316003"
---
# <a name="txtwidth-cell-text-transform-section"></a><span data-ttu-id="49eca-104">[TxtWidth] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="49eca-104">TxtWidth Cell (Text Transform Section)</span></span>

<span data-ttu-id="49eca-105">テキスト ブロックの幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="49eca-105">Determines the width of the text block.</span></span> <span data-ttu-id="49eca-106">既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="49eca-106">The default formula is:</span></span>
  
<span data-ttu-id="49eca-107">= 幅\* 1</span><span class="sxs-lookup"><span data-stu-id="49eca-107">= Width \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="49eca-108">解説</span><span class="sxs-lookup"><span data-stu-id="49eca-108">Remarks</span></span>

<span data-ttu-id="49eca-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtWidth] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="49eca-109">To get a reference to the TxtWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="49eca-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="49eca-110">Cell name:</span></span>  <br/> | <span data-ttu-id="49eca-111">[txtwidth]</span><span class="sxs-lookup"><span data-stu-id="49eca-111">TxtWidth</span></span>  <br/> |
   
<span data-ttu-id="49eca-112">プログラムから、インデックスによって [TxtWidth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="49eca-112">To get a reference to the TxtWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="49eca-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="49eca-113">Section index:</span></span>  <br/> |<span data-ttu-id="49eca-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="49eca-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="49eca-115">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="49eca-115">Row index:</span></span>  <br/> |<span data-ttu-id="49eca-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="49eca-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="49eca-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="49eca-117">Cell index:</span></span>  <br/> |<span data-ttu-id="49eca-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="49eca-118">**visXFormWidth**</span></span> <br/> |
   

