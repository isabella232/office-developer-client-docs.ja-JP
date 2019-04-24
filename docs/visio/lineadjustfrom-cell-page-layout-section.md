---
title: '[LineAdjustFrom] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: 複数の動的コネクタが迂回する場合に、線を分離するコネクタを指定します。
ms.openlocfilehash: 3eb9f5513ee3ce2f5dce96cb47c356bca29a289c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359326"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="0d0fc-103">[LineAdjustFrom] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="0d0fc-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="0d0fc-104">複数の動的コネクタが迂回する場合に、線を分離するコネクタを指定します。</span><span class="sxs-lookup"><span data-stu-id="0d0fc-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="0d0fc-105">**値**</span><span class="sxs-lookup"><span data-stu-id="0d0fc-105">**Value**</span></span>|<span data-ttu-id="0d0fc-106">**セレクター**</span><span class="sxs-lookup"><span data-stu-id="0d0fc-106">**Adjustment**</span></span>|<span data-ttu-id="0d0fc-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="0d0fc-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0d0fc-108">.0</span><span class="sxs-lookup"><span data-stu-id="0d0fc-108">0</span></span>  <br/> |<span data-ttu-id="0d0fc-109">関連付けられていない線</span><span class="sxs-lookup"><span data-stu-id="0d0fc-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="0d0fc-110">**visPLOLineAdjustFromNotRelated**</span><span class="sxs-lookup"><span data-stu-id="0d0fc-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="0d0fc-111">1-d</span><span class="sxs-lookup"><span data-stu-id="0d0fc-111">1</span></span>  <br/> |<span data-ttu-id="0d0fc-112">すべての線</span><span class="sxs-lookup"><span data-stu-id="0d0fc-112">All lines</span></span>  <br/> |<span data-ttu-id="0d0fc-113">**visPLOLineAdjustFromAll**</span><span class="sxs-lookup"><span data-stu-id="0d0fc-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="0d0fc-114">pbm-2</span><span class="sxs-lookup"><span data-stu-id="0d0fc-114">2</span></span>  <br/> |<span data-ttu-id="0d0fc-115">なし</span><span class="sxs-lookup"><span data-stu-id="0d0fc-115">No lines</span></span>  <br/> |<span data-ttu-id="0d0fc-116">**visPLOLineAdjustFromNone**</span><span class="sxs-lookup"><span data-stu-id="0d0fc-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="0d0fc-117">1/3</span><span class="sxs-lookup"><span data-stu-id="0d0fc-117">3</span></span>  <br/> |<span data-ttu-id="0d0fc-118">迂回方法の既定値に合わせる</span><span class="sxs-lookup"><span data-stu-id="0d0fc-118">Routing style default</span></span>  <br/> |<span data-ttu-id="0d0fc-119">**visPLOLineAdjustFromRoutingDefault**</span><span class="sxs-lookup"><span data-stu-id="0d0fc-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d0fc-120">解説</span><span class="sxs-lookup"><span data-stu-id="0d0fc-120">Remarks</span></span>

<span data-ttu-id="0d0fc-121">このセルの値は、[**ページ設定**] ダイアログ ボックスの [**レイアウトと経路**] タブで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックして、[**レイアウトと経路**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="0d0fc-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="0d0fc-122">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineAdjustFrom] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0d0fc-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d0fc-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="0d0fc-123">Cell name:</span></span>  <br/> |<span data-ttu-id="0d0fc-124">[lineadjustfrom]</span><span class="sxs-lookup"><span data-stu-id="0d0fc-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="0d0fc-125">プログラムから、インデックスによって [LineAdjustFrom] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d0fc-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d0fc-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0d0fc-126">Section index:</span></span>  <br/> |<span data-ttu-id="0d0fc-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0d0fc-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0d0fc-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0d0fc-128">Row index:</span></span>  <br/> |<span data-ttu-id="0d0fc-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="0d0fc-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="0d0fc-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0d0fc-130">Cell index:</span></span>  <br/> |<span data-ttu-id="0d0fc-131">**visPLOLineAdjustFrom**</span><span class="sxs-lookup"><span data-stu-id="0d0fc-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

