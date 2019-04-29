---
title: '[KeepTextFlat] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: 図形のテキストが3-d 図形の回転を無視するかどうかを示します。 2-D 回転には適用されません。
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422041"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a><span data-ttu-id="1c54f-104">[KeepTextFlat] セル ([3-D 回転のプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="1c54f-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="1c54f-105">図形のテキストが3-d 図形の回転を無視するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="1c54f-105">Indicates whether a shape's text will ignore the shape's rotation in 3-D.</span></span> <span data-ttu-id="1c54f-106">2-D 回転には適用されません。</span><span class="sxs-lookup"><span data-stu-id="1c54f-106">Does not apply to 2-D rotation.</span></span> 
  
****

|<span data-ttu-id="1c54f-107">**値**</span><span class="sxs-lookup"><span data-stu-id="1c54f-107">**Value**</span></span>|<span data-ttu-id="1c54f-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="1c54f-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1c54f-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="1c54f-109">TRUE</span></span>  <br/> |<span data-ttu-id="1c54f-110">図形のテキストは、図形の座標を使用して回転しません。</span><span class="sxs-lookup"><span data-stu-id="1c54f-110">Shape text does not rotate with the shape's geometry.</span></span>  <br/> |
|<span data-ttu-id="1c54f-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="1c54f-111">FALSE</span></span>  <br/> |<span data-ttu-id="1c54f-112">図形のテキストは、図形の座標を使用して回転するように変換されます。</span><span class="sxs-lookup"><span data-stu-id="1c54f-112">Shape text is transformed to rotate with the shape's geometry.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c54f-113">注釈</span><span class="sxs-lookup"><span data-stu-id="1c54f-113">Remarks</span></span>

<span data-ttu-id="1c54f-114">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**KeepTextFlat**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1c54f-114">To get a reference to the **KeepTextFlat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c54f-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="1c54f-115">Cell name:</span></span>  <br/> |<span data-ttu-id="1c54f-116">[keeptextflat]</span><span class="sxs-lookup"><span data-stu-id="1c54f-116">KeepTextFlat</span></span>  <br/> |
   
<span data-ttu-id="1c54f-117">プログラムから、インデックスによって [**KeepTextFlat**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1c54f-117">To get a reference to the **KeepTextFlat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c54f-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1c54f-118">Section index:</span></span>  <br/> |<span data-ttu-id="1c54f-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1c54f-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1c54f-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1c54f-120">Row index:</span></span>  <br/> |<span data-ttu-id="1c54f-121">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="1c54f-121">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="1c54f-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1c54f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="1c54f-123">**visKeepTextFlat**</span><span class="sxs-lookup"><span data-stu-id="1c54f-123">**visKeepTextFlat**</span></span> <br/> |
   

