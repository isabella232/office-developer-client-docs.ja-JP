---
title: '[TxtPinX] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: X を決定するが、テキスト ブロックの図形の原点を基準として回転の中心の座標です。 既定の数式は次のとおりです。
ms.openlocfilehash: df103557d103dbde7e4a1c8d67cabe37a0af9311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806701"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="932ba-104">[TxtPinX] セル ([テキスト変換] セクション)</span><span class="sxs-lookup"><span data-stu-id="932ba-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="932ba-105">*X*の決定に、テキスト ブロックの図形の原点を基準として回転の中心の座標。</span><span class="sxs-lookup"><span data-stu-id="932ba-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="932ba-106">既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="932ba-106">The default formula is:</span></span> 
  
<span data-ttu-id="932ba-107">= 幅\*0.5</span><span class="sxs-lookup"><span data-stu-id="932ba-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="932ba-108">注釈</span><span class="sxs-lookup"><span data-stu-id="932ba-108">Remarks</span></span>

<span data-ttu-id="932ba-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtPinX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="932ba-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="932ba-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="932ba-110">Cell name:</span></span>  <br/> | <span data-ttu-id="932ba-111">[Txtpinx]</span><span class="sxs-lookup"><span data-stu-id="932ba-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="932ba-112">プログラムから、インデックスによって [TxtPinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="932ba-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="932ba-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="932ba-113">Section index:</span></span>  <br/> |<span data-ttu-id="932ba-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="932ba-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="932ba-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="932ba-115">Row index:</span></span>  <br/> |<span data-ttu-id="932ba-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="932ba-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="932ba-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="932ba-117">Cell index:</span></span>  <br/> |<span data-ttu-id="932ba-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="932ba-118">**visXFormPinX**</span></span> <br/> |
   

