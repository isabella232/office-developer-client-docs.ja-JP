---
title: '[TxtAngle] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251272
localization_priority: Normal
ms.assetid: b8482cd8-5205-40ef-b4e1-4ceb197ac80f
description: テキスト ブロックの現在の x を基準にして回転角度を指定の形状の軸です。 既定値は、0 度です。
ms.openlocfilehash: 08ed4422392a355db948fa947abdfd3772dec0a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806695"
---
# <a name="txtangle-cell-text-transform-section"></a><span data-ttu-id="4fef1-104">[TxtAngle] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="4fef1-104">TxtAngle Cell (Text Transform Section)</span></span>

<span data-ttu-id="4fef1-105">テキスト ブロックの現在の*x*を基準にして回転角度を指定の形状の軸です。</span><span class="sxs-lookup"><span data-stu-id="4fef1-105">Determines the text block's current angle of rotation in relation to the  *x*  -axis of the shape.</span></span> <span data-ttu-id="4fef1-106">既定値は、0 度です。</span><span class="sxs-lookup"><span data-stu-id="4fef1-106">The default is 0 degrees.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4fef1-107">備考</span><span class="sxs-lookup"><span data-stu-id="4fef1-107">Remarks</span></span>

<span data-ttu-id="4fef1-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [txtangle] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="4fef1-108">To get a reference to the TxtAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4fef1-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="4fef1-109">Cell name:</span></span>  <br/> | <span data-ttu-id="4fef1-110">[Txtangle]</span><span class="sxs-lookup"><span data-stu-id="4fef1-110">TxtAngle</span></span>  <br/> |
   
<span data-ttu-id="4fef1-111">プログラムから、インデックスによって [txtangle] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="4fef1-111">To get a reference to the TxtAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4fef1-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4fef1-112">Section index:</span></span>  <br/> |<span data-ttu-id="4fef1-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4fef1-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4fef1-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4fef1-114">Row index:</span></span>  <br/> |<span data-ttu-id="4fef1-115">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="4fef1-115">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="4fef1-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4fef1-116">Cell index:</span></span>  <br/> |<span data-ttu-id="4fef1-117">**visXFormAngle**</span><span class="sxs-lookup"><span data-stu-id="4fef1-117">**visXFormAngle**</span></span> <br/> |
   

