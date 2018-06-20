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
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="20aec-104">[TxtPinX] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="20aec-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="20aec-105">*X*の決定に、テキスト ブロックの図形の原点を基準として回転の中心の座標。</span><span class="sxs-lookup"><span data-stu-id="20aec-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="20aec-106">既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="20aec-106">The default formula is:</span></span> 
  
<span data-ttu-id="20aec-107">= 幅\*0.5</span><span class="sxs-lookup"><span data-stu-id="20aec-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20aec-108">備考</span><span class="sxs-lookup"><span data-stu-id="20aec-108">Remarks</span></span>

<span data-ttu-id="20aec-109">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [txtpinx] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="20aec-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20aec-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="20aec-110">Cell name:</span></span>  <br/> | <span data-ttu-id="20aec-111">[Txtpinx]</span><span class="sxs-lookup"><span data-stu-id="20aec-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="20aec-112">プログラムから、インデックスによって [txtpinx] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="20aec-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20aec-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="20aec-113">Section index:</span></span>  <br/> |<span data-ttu-id="20aec-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="20aec-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="20aec-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="20aec-115">Row index:</span></span>  <br/> |<span data-ttu-id="20aec-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="20aec-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="20aec-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="20aec-117">Cell index:</span></span>  <br/> |<span data-ttu-id="20aec-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="20aec-118">**visXFormPinX**</span></span> <br/> |
   

