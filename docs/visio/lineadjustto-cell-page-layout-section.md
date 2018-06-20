---
title: '[LineAdjustTo] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: 線を束ねるときに対象とする動的コネクタを指定します。
ms.openlocfilehash: 13540f9dc5e6e6861d3f3679bcf49204d553397a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805701"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="6f16c-103">[LineAdjustTo] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="6f16c-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="6f16c-104">線を束ねるときに対象とする動的コネクタを指定します。</span><span class="sxs-lookup"><span data-stu-id="6f16c-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="6f16c-105">**値**</span><span class="sxs-lookup"><span data-stu-id="6f16c-105">**Value**</span></span>|<span data-ttu-id="6f16c-106">**調整**</span><span class="sxs-lookup"><span data-stu-id="6f16c-106">**Adjustment**</span></span>|<span data-ttu-id="6f16c-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="6f16c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6f16c-108">0</span><span class="sxs-lookup"><span data-stu-id="6f16c-108">0</span></span>  <br/> |<span data-ttu-id="6f16c-109">迂回方法の既定値に合わせる</span><span class="sxs-lookup"><span data-stu-id="6f16c-109">Routing style default</span></span>  <br/> |<span data-ttu-id="6f16c-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="6f16c-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="6f16c-111">1</span><span class="sxs-lookup"><span data-stu-id="6f16c-111">1</span></span>  <br/> |<span data-ttu-id="6f16c-112">近接しているすべての線</span><span class="sxs-lookup"><span data-stu-id="6f16c-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="6f16c-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="6f16c-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="6f16c-114">2</span><span class="sxs-lookup"><span data-stu-id="6f16c-114">2</span></span>  <br/> |<span data-ttu-id="6f16c-115">なし</span><span class="sxs-lookup"><span data-stu-id="6f16c-115">No lines</span></span>  <br/> |<span data-ttu-id="6f16c-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="6f16c-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="6f16c-117">3</span><span class="sxs-lookup"><span data-stu-id="6f16c-117">3</span></span>  <br/> |<span data-ttu-id="6f16c-118">関連付けられている線</span><span class="sxs-lookup"><span data-stu-id="6f16c-118">Related lines</span></span>  <br/> |<span data-ttu-id="6f16c-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="6f16c-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f16c-120">備考</span><span class="sxs-lookup"><span data-stu-id="6f16c-120">Remarks</span></span>

<span data-ttu-id="6f16c-121">**[ページ設定**] ダイアログ ボックスで、[**レイアウトと経路**] タブで、このセルの値を設定することもできます ([**デザイン**] タブで、 **[ページ設定**の矢印をクリックし、[**レイアウトと経路**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="6f16c-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="6f16c-122">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineAdjustTo] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="6f16c-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6f16c-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="6f16c-123">Cell name:</span></span>  <br/> |<span data-ttu-id="6f16c-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="6f16c-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="6f16c-125">プログラムから、インデックスによって [LineAdjustTo] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="6f16c-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6f16c-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6f16c-126">Section index:</span></span>  <br/> |<span data-ttu-id="6f16c-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6f16c-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6f16c-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6f16c-128">Row index:</span></span>  <br/> |<span data-ttu-id="6f16c-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="6f16c-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="6f16c-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6f16c-130">Cell index:</span></span>  <br/> |<span data-ttu-id="6f16c-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="6f16c-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

