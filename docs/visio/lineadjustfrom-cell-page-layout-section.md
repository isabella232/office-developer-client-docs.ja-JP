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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415188"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="6bbd0-103">[LineAdjustFrom] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="6bbd0-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="6bbd0-104">複数の動的コネクタが迂回する場合に、線を分離するコネクタを指定します。</span><span class="sxs-lookup"><span data-stu-id="6bbd0-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="6bbd0-105">**値**</span><span class="sxs-lookup"><span data-stu-id="6bbd0-105">**Value**</span></span>|<span data-ttu-id="6bbd0-106">**調整**</span><span class="sxs-lookup"><span data-stu-id="6bbd0-106">**Adjustment**</span></span>|<span data-ttu-id="6bbd0-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="6bbd0-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6bbd0-108">0</span><span class="sxs-lookup"><span data-stu-id="6bbd0-108">0</span></span>  <br/> |<span data-ttu-id="6bbd0-109">関連付けられていない線</span><span class="sxs-lookup"><span data-stu-id="6bbd0-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="6bbd0-110">**visPLOLineAdjustFromNotRelated**</span><span class="sxs-lookup"><span data-stu-id="6bbd0-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="6bbd0-111">1</span><span class="sxs-lookup"><span data-stu-id="6bbd0-111">1</span></span>  <br/> |<span data-ttu-id="6bbd0-112">すべての線</span><span class="sxs-lookup"><span data-stu-id="6bbd0-112">All lines</span></span>  <br/> |<span data-ttu-id="6bbd0-113">**visPLOLineAdjustFromAll**</span><span class="sxs-lookup"><span data-stu-id="6bbd0-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="6bbd0-114">2</span><span class="sxs-lookup"><span data-stu-id="6bbd0-114">2</span></span>  <br/> |<span data-ttu-id="6bbd0-115">なし</span><span class="sxs-lookup"><span data-stu-id="6bbd0-115">No lines</span></span>  <br/> |<span data-ttu-id="6bbd0-116">**visPLOLineAdjustFromNone**</span><span class="sxs-lookup"><span data-stu-id="6bbd0-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="6bbd0-117">3</span><span class="sxs-lookup"><span data-stu-id="6bbd0-117">3</span></span>  <br/> |<span data-ttu-id="6bbd0-118">迂回方法の既定値に合わせる</span><span class="sxs-lookup"><span data-stu-id="6bbd0-118">Routing style default</span></span>  <br/> |<span data-ttu-id="6bbd0-119">**visPLOLineAdjustFromRoutingDefault**</span><span class="sxs-lookup"><span data-stu-id="6bbd0-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6bbd0-120">注釈</span><span class="sxs-lookup"><span data-stu-id="6bbd0-120">Remarks</span></span>

<span data-ttu-id="6bbd0-121">このセルの値は、[**ページ設定**] ダイアログ ボックスの [**レイアウトと経路**] タブで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックして、[**レイアウトと経路**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="6bbd0-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="6bbd0-122">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineAdjustFrom] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6bbd0-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6bbd0-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="6bbd0-123">Cell name:</span></span>  <br/> |<span data-ttu-id="6bbd0-124">LineAdjustFrom</span><span class="sxs-lookup"><span data-stu-id="6bbd0-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="6bbd0-125">プログラムから、インデックスによって [LineAdjustFrom] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6bbd0-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6bbd0-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6bbd0-126">Section index:</span></span>  <br/> |<span data-ttu-id="6bbd0-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6bbd0-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6bbd0-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6bbd0-128">Row index:</span></span>  <br/> |<span data-ttu-id="6bbd0-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="6bbd0-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="6bbd0-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6bbd0-130">Cell index:</span></span>  <br/> |<span data-ttu-id="6bbd0-131">**visPLOLineAdjustFrom**</span><span class="sxs-lookup"><span data-stu-id="6bbd0-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

