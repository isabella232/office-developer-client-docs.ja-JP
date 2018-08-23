---
title: '[LocPinX] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: X を表す-図形の原点を基準として、図形の pin (回転の中心) の座標。 [Locpinx] を決定するための既定の数式は次のとおりです。
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805802"
---
# <a name="locpinx-cell-shape-transform-section"></a><span data-ttu-id="be0ce-104">[LocPinX] セル ([図形変換] セクション)</span><span class="sxs-lookup"><span data-stu-id="be0ce-104">LocPinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="be0ce-105">*X*を表す-図形の原点を基準として、図形の pin (回転の中心) の座標。</span><span class="sxs-lookup"><span data-stu-id="be0ce-105">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="be0ce-106">[Locpinx] を決定するための既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="be0ce-106">The default formula for determining LocPinX is:</span></span> 
  
<span data-ttu-id="be0ce-107">= 幅\*0.5</span><span class="sxs-lookup"><span data-stu-id="be0ce-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="be0ce-108">注釈</span><span class="sxs-lookup"><span data-stu-id="be0ce-108">Remarks</span></span>

<span data-ttu-id="be0ce-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LocPinX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="be0ce-109">To get a reference to the LocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be0ce-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="be0ce-110">Cell name:</span></span>  <br/> | <span data-ttu-id="be0ce-111">[Locpinx]</span><span class="sxs-lookup"><span data-stu-id="be0ce-111">LocPinX</span></span>  <br/> |
   
<span data-ttu-id="be0ce-112">プログラムから、インデックスによって [LocPinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="be0ce-112">To get a reference to the LocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be0ce-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="be0ce-113">Section index:</span></span>  <br/> |<span data-ttu-id="be0ce-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="be0ce-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="be0ce-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="be0ce-115">Row index:</span></span>  <br/> |<span data-ttu-id="be0ce-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="be0ce-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="be0ce-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="be0ce-117">Cell index:</span></span>  <br/> |<span data-ttu-id="be0ce-118">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="be0ce-118">**visXFormLocPinX**</span></span> <br/> |
   

