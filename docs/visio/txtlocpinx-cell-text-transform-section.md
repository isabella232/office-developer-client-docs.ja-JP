---
title: '[TxtLocPinX] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: X の決定に、テキスト ブロックのテキスト ブロックの原点を基準として回転の中心の座標。 既定の数式は次のとおりです。
ms.openlocfilehash: 6eb48532bb19bce5b0d22ed2cd0997014721df88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806690"
---
# <a name="txtlocpinx-cell-text-transform-section"></a><span data-ttu-id="bedb9-104">[TxtLocPinX] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="bedb9-104">TxtLocPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="bedb9-105">*X*が決まりますが、テキスト ブロックのテキスト ブロックの原点を基準として回転の中心の座標。</span><span class="sxs-lookup"><span data-stu-id="bedb9-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the text block.</span></span> <span data-ttu-id="bedb9-106">既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bedb9-106">The default formula is:</span></span> 
  
<span data-ttu-id="bedb9-107">= [Txtwidth] \* 0.5</span><span class="sxs-lookup"><span data-stu-id="bedb9-107">= TxtWidth \* 0.5</span></span>
  
<span data-ttu-id="bedb9-108">この数式では、テキスト ブロックの水平方向の中心が回転の中心になります。</span><span class="sxs-lookup"><span data-stu-id="bedb9-108">This formula evaluates to the horizontal center of the text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bedb9-109">備考</span><span class="sxs-lookup"><span data-stu-id="bedb9-109">Remarks</span></span>

<span data-ttu-id="bedb9-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[TxtLocPinX] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="bedb9-110">To get a reference to the TxtLocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bedb9-111">セル名 :</span><span class="sxs-lookup"><span data-stu-id="bedb9-111">Cell name:</span></span>  <br/> | <span data-ttu-id="bedb9-112">TxtLocPinX</span><span class="sxs-lookup"><span data-stu-id="bedb9-112">TxtLocPinX</span></span>  <br/> |
   
<span data-ttu-id="bedb9-113">プログラムから、インデックスによって [TxtLocPinX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="bedb9-113">To get a reference to the TxtLocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bedb9-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bedb9-114">Section index:</span></span>  <br/> |<span data-ttu-id="bedb9-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bedb9-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bedb9-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bedb9-116">Row index:</span></span>  <br/> |<span data-ttu-id="bedb9-117">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="bedb9-117">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="bedb9-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bedb9-118">Cell index:</span></span>  <br/> |<span data-ttu-id="bedb9-119">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="bedb9-119">**visXFormLocPinX**</span></span> <br/> |
   

