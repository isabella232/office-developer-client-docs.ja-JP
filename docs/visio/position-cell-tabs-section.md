---
title: '[Position] セル ([Tabs] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: タブ位置を指定します。タブ位置は図面の縮尺による影響を受けません。図面の縮尺を変更しても、タブ位置は変わりません。
ms.openlocfilehash: 06f3a9fd5cfdf78f5383e70f32f8514b0adab114
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806104"
---
# <a name="position-cell-tabs-section"></a><span data-ttu-id="27e59-105">[Position] セル ([Tabs] セクション)</span><span class="sxs-lookup"><span data-stu-id="27e59-105">Position Cell (Tabs Section)</span></span>

<span data-ttu-id="27e59-p102">タブ位置を指定します。タブ位置は図面の縮尺による影響を受けません。図面の縮尺を変更しても、タブ位置は変わりません。</span><span class="sxs-lookup"><span data-stu-id="27e59-p102">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27e59-109">備考</span><span class="sxs-lookup"><span data-stu-id="27e59-109">Remarks</span></span>

<span data-ttu-id="27e59-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって Position] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="27e59-110">To get a reference to the Position cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27e59-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="27e59-111">Cell name:</span></span>  <br/> | <span data-ttu-id="27e59-112">タブします。</span><span class="sxs-lookup"><span data-stu-id="27e59-112">Tabs.</span></span>  <span data-ttu-id="27e59-113">*ij* 、 *i*および*j* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="27e59-113">*ij*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="27e59-114">プログラムから、インデックスによって [Position] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="27e59-114">To get a reference to the Position cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27e59-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="27e59-115">Section index:</span></span>  <br/> |<span data-ttu-id="27e59-116">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="27e59-116">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="27e59-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="27e59-117">Row index:</span></span>  <br/> |<span data-ttu-id="27e59-118">**visRowTab** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="27e59-118">**visRowTab** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="27e59-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="27e59-119">Cell index:</span></span>  <br/> | <span data-ttu-id="27e59-120">(*j* \* 3) + **visTabPos**</span><span class="sxs-lookup"><span data-stu-id="27e59-120">(*j*  \*3) + **visTabPos**</span></span> <br/> |
   

