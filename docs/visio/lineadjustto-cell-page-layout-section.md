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
ms.openlocfilehash: e4fb32c0fcb488173324ea597edc2c9d13f6bfca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414026"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="52554-103">[LineAdjustTo] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="52554-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="52554-104">線を束ねるときに対象とする動的コネクタを指定します。</span><span class="sxs-lookup"><span data-stu-id="52554-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="52554-105">**値**</span><span class="sxs-lookup"><span data-stu-id="52554-105">**Value**</span></span>|<span data-ttu-id="52554-106">**調整**</span><span class="sxs-lookup"><span data-stu-id="52554-106">**Adjustment**</span></span>|<span data-ttu-id="52554-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="52554-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="52554-108">0</span><span class="sxs-lookup"><span data-stu-id="52554-108">0</span></span>  <br/> |<span data-ttu-id="52554-109">迂回方法の既定値に合わせる</span><span class="sxs-lookup"><span data-stu-id="52554-109">Routing style default</span></span>  <br/> |<span data-ttu-id="52554-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="52554-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="52554-111">1</span><span class="sxs-lookup"><span data-stu-id="52554-111">1</span></span>  <br/> |<span data-ttu-id="52554-112">近接しているすべての線</span><span class="sxs-lookup"><span data-stu-id="52554-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="52554-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="52554-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="52554-114">2</span><span class="sxs-lookup"><span data-stu-id="52554-114">2</span></span>  <br/> |<span data-ttu-id="52554-115">なし</span><span class="sxs-lookup"><span data-stu-id="52554-115">No lines</span></span>  <br/> |<span data-ttu-id="52554-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="52554-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="52554-117">3</span><span class="sxs-lookup"><span data-stu-id="52554-117">3</span></span>  <br/> |<span data-ttu-id="52554-118">関連付けられている線</span><span class="sxs-lookup"><span data-stu-id="52554-118">Related lines</span></span>  <br/> |<span data-ttu-id="52554-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="52554-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52554-120">注釈</span><span class="sxs-lookup"><span data-stu-id="52554-120">Remarks</span></span>

<span data-ttu-id="52554-121">このセルの値は、[**ページ設定**] ダイアログ ボックスの [**レイアウトと経路**] タブで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックして、[**レイアウトと経路**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="52554-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="52554-122">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineAdjustTo] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="52554-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52554-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="52554-123">Cell name:</span></span>  <br/> |<span data-ttu-id="52554-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="52554-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="52554-125">プログラムから、インデックスによって [LineAdjustTo] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="52554-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52554-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="52554-126">Section index:</span></span>  <br/> |<span data-ttu-id="52554-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="52554-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="52554-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="52554-128">Row index:</span></span>  <br/> |<span data-ttu-id="52554-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="52554-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="52554-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="52554-130">Cell index:</span></span>  <br/> |<span data-ttu-id="52554-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="52554-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

