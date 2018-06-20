---
title: '[NoQuickDrag] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: 図形の選択またはユーザーは、[Geometry] セクションで定義されている塗りつぶしの領域をクリックしたときにドラッグするかどうかを決定します。
ms.openlocfilehash: 7d4ffd876d8676af885b8f750fecf6f6d0deaa9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805932"
---
# <a name="noquickdrag-cell-geometry-section"></a><span data-ttu-id="af324-103">[NoQuickDrag] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="af324-103">NoQuickDrag Cell (Geometry Section)</span></span>

<span data-ttu-id="af324-104">図形の選択またはユーザーは、[Geometry] セクションで定義されている塗りつぶしの領域をクリックしたときにドラッグするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="af324-104">Determines whether a shape can be selected or dragged when the user clicks the filled area defined by the Geometry section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af324-105">備考</span><span class="sxs-lookup"><span data-stu-id="af324-105">Remarks</span></span>

<span data-ttu-id="af324-106">参照を取得する NoQuickDrag のセルに名前を別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="af324-106">To get a reference to the NoQuickDrag cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af324-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="af324-107">Cell name:</span></span>  <br/> |<span data-ttu-id="af324-108">ジオメトリの*i*です。NoQuickDrag、* i * - < 1 > 2、3.</span><span class="sxs-lookup"><span data-stu-id="af324-108">Geometry  *i*  .NoQuickDrag, where  * i *  - <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="af324-109">プログラムから、インデックスによって [NoQuickDrag] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="af324-109">To get a reference to the NoQuickDrag cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af324-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="af324-110">Section index:</span></span>  <br/> |<span data-ttu-id="af324-111">**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="af324-111">**visSectionFirstComponent** +  *i*  , where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="af324-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="af324-112">Row index:</span></span>  <br/> |<span data-ttu-id="af324-113">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="af324-113">**visRowComponent**</span></span> <br/> |
|<span data-ttu-id="af324-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="af324-114">Cell index:</span></span>  <br/> |<span data-ttu-id="af324-115">**visCompNoQuickDrag**</span><span class="sxs-lookup"><span data-stu-id="af324-115">**visCompNoQuickDrag**</span></span> <br/> |
   

