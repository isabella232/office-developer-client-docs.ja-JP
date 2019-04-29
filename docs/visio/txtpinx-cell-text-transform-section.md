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
description: 図形の原点を基準にして、テキストブロックの回転中心の x 座標を指定します。 既定の数式は次のとおりです。
ms.openlocfilehash: 836f5c807d0c0e53efc825f62f60429274282165
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423497"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="e7fd8-104">[TxtPinX] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="e7fd8-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="e7fd8-105">図形の原点を基準にして、テキストブロックの回転中心の*x*座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7fd8-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="e7fd8-106">既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e7fd8-106">The default formula is:</span></span> 
  
<span data-ttu-id="e7fd8-107">= 幅\* 0.5</span><span class="sxs-lookup"><span data-stu-id="e7fd8-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7fd8-108">注釈</span><span class="sxs-lookup"><span data-stu-id="e7fd8-108">Remarks</span></span>

<span data-ttu-id="e7fd8-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtPinX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e7fd8-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e7fd8-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="e7fd8-110">Cell name:</span></span>  <br/> | <span data-ttu-id="e7fd8-111">[txtpinx]</span><span class="sxs-lookup"><span data-stu-id="e7fd8-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="e7fd8-112">プログラムから、インデックスによって [TxtPinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7fd8-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e7fd8-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e7fd8-113">Section index:</span></span>  <br/> |<span data-ttu-id="e7fd8-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e7fd8-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e7fd8-115">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="e7fd8-115">Row index:</span></span>  <br/> |<span data-ttu-id="e7fd8-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="e7fd8-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="e7fd8-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e7fd8-117">Cell index:</span></span>  <br/> |<span data-ttu-id="e7fd8-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="e7fd8-118">**visXFormPinX**</span></span> <br/> |
   

