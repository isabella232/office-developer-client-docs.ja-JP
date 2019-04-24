---
title: '[DefaultTabstop] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
localization_priority: Normal
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: テキスト ブロックの既定のタブ位置の間隔を指定します。
ms.openlocfilehash: 1ae923f6373b9cee76238b1fb27ec5eb3acb43ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360271"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a><span data-ttu-id="ff442-103">[DefaultTabstop] セル ([Text Block Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="ff442-103">DefaultTabstop Cell (Text Block Format Section)</span></span>

<span data-ttu-id="ff442-104">テキスト ブロックの既定のタブ位置の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="ff442-104">Determines the interval of the default tab stops in a text block.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ff442-105">解説</span><span class="sxs-lookup"><span data-stu-id="ff442-105">Remarks</span></span>

<span data-ttu-id="ff442-106">既定値は、英国単位で図面を作成した場合は 0.5 インチ、メートル法単位の場合は 1.5 cm になります。</span><span class="sxs-lookup"><span data-stu-id="ff442-106">The default value is 0.5 inches for documents created in imperial units and 1.5 centimeters for documents created in metric units.</span></span>
  
<span data-ttu-id="ff442-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DefaultTabstop] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ff442-107">To get a reference to the DefaultTabstop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff442-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="ff442-108">Cell name:</span></span>  <br/> |<span data-ttu-id="ff442-109">DefaultTabstop</span><span class="sxs-lookup"><span data-stu-id="ff442-109">DefaultTabstop</span></span>  <br/> |
   
<span data-ttu-id="ff442-110">プログラムから、インデックスによって [DefaultTabstop] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ff442-110">To get a reference to the DefaultTabstop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff442-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ff442-111">Section index:</span></span>  <br/> |<span data-ttu-id="ff442-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ff442-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ff442-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ff442-113">Row index:</span></span>  <br/> |<span data-ttu-id="ff442-114">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="ff442-114">**visRowText**</span></span> <br/> |
|<span data-ttu-id="ff442-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ff442-115">Cell index:</span></span>  <br/> |<span data-ttu-id="ff442-116">**visTxtBlkDefaultTabStop**</span><span class="sxs-lookup"><span data-stu-id="ff442-116">**visTxtBlkDefaultTabStop**</span></span> <br/> |
   

