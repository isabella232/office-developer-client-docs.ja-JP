---
title: '[RightMargin] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: テキスト ブロックの右の枠線と、そのブロックに含まれるテキストとの間隔を指定します。既定値は 0.1 インチです。
ms.openlocfilehash: 57fdb320395a9a6562983a0148b37c4a70a9a9b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806236"
---
# <a name="rightmargin-cell-text-block-format-section"></a><span data-ttu-id="fe804-104">[RightMargin] セル ([Text Block Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="fe804-104">RightMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="fe804-p102">テキスト ブロックの右の枠線と、そのブロックに含まれるテキストとの間隔を指定します。既定値は 0.1 インチです。</span><span class="sxs-lookup"><span data-stu-id="fe804-p102">Determines the distance between the right border of the text block and the text it contains. The default is 0.1 inch.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe804-107">備考</span><span class="sxs-lookup"><span data-stu-id="fe804-107">Remarks</span></span>

<span data-ttu-id="fe804-p103">この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、右余白は変わりません。</span><span class="sxs-lookup"><span data-stu-id="fe804-p103">This value is independent of the scale of the drawing. If the drawing is scaled, the right margin remains the same.</span></span>
  
<span data-ttu-id="fe804-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって RightMargin] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="fe804-110">To get a reference to the RightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe804-111">セル名 :</span><span class="sxs-lookup"><span data-stu-id="fe804-111">Cell name:</span></span>  <br/> | <span data-ttu-id="fe804-112">右マージン</span><span class="sxs-lookup"><span data-stu-id="fe804-112">RightMargin</span></span>  <br/> |
   
<span data-ttu-id="fe804-113">プログラムから、インデックスによって [RightMargin] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="fe804-113">To get a reference to the RightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe804-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fe804-114">Section index:</span></span>  <br/> |<span data-ttu-id="fe804-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fe804-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fe804-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fe804-116">Row index:</span></span>  <br/> |<span data-ttu-id="fe804-117">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="fe804-117">**visRowText**</span></span> <br/> |
| <span data-ttu-id="fe804-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fe804-118">Cell index:</span></span>  <br/> |<span data-ttu-id="fe804-119">**visTxtBlkRightMargin**</span><span class="sxs-lookup"><span data-stu-id="fe804-119">**visTxtBlkRightMargin**</span></span> <br/> |
   

