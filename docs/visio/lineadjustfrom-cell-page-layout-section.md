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
ms.openlocfilehash: ee3a107f7e19b53017c2ea24c94babceb49620d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805690"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="19392-103">[LineAdjustFrom] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="19392-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="19392-104">複数の動的コネクタが迂回する場合に、線を分離するコネクタを指定します。</span><span class="sxs-lookup"><span data-stu-id="19392-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="19392-105">**値**</span><span class="sxs-lookup"><span data-stu-id="19392-105">**Value**</span></span>|<span data-ttu-id="19392-106">**調整**</span><span class="sxs-lookup"><span data-stu-id="19392-106">**Adjustment**</span></span>|<span data-ttu-id="19392-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="19392-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="19392-108">0</span><span class="sxs-lookup"><span data-stu-id="19392-108">0</span></span>  <br/> |<span data-ttu-id="19392-109">関連付けられていない線</span><span class="sxs-lookup"><span data-stu-id="19392-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="19392-110">**visPLOLineAdjustFromNotRelated**</span><span class="sxs-lookup"><span data-stu-id="19392-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="19392-111">1</span><span class="sxs-lookup"><span data-stu-id="19392-111">1</span></span>  <br/> |<span data-ttu-id="19392-112">すべての線</span><span class="sxs-lookup"><span data-stu-id="19392-112">All lines</span></span>  <br/> |<span data-ttu-id="19392-113">**visPLOLineAdjustFromAll**</span><span class="sxs-lookup"><span data-stu-id="19392-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="19392-114">2</span><span class="sxs-lookup"><span data-stu-id="19392-114">2</span></span>  <br/> |<span data-ttu-id="19392-115">なし</span><span class="sxs-lookup"><span data-stu-id="19392-115">No lines</span></span>  <br/> |<span data-ttu-id="19392-116">**visPLOLineAdjustFromNone**</span><span class="sxs-lookup"><span data-stu-id="19392-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="19392-117">3</span><span class="sxs-lookup"><span data-stu-id="19392-117">3</span></span>  <br/> |<span data-ttu-id="19392-118">迂回方法の既定値に合わせる</span><span class="sxs-lookup"><span data-stu-id="19392-118">Routing style default</span></span>  <br/> |<span data-ttu-id="19392-119">**visPLOLineAdjustFromRoutingDefault**</span><span class="sxs-lookup"><span data-stu-id="19392-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19392-120">備考</span><span class="sxs-lookup"><span data-stu-id="19392-120">Remarks</span></span>

<span data-ttu-id="19392-121">**[ページ設定**] ダイアログ ボックスで、[**レイアウトと経路**] タブで、このセルの値を設定することもできます ([**デザイン**] タブで、 **[ページ設定**の矢印をクリックし、[**レイアウトと経路**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="19392-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="19392-122">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineAdjustFrom] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="19392-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19392-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="19392-123">Cell name:</span></span>  <br/> |<span data-ttu-id="19392-124">LineAdjustFrom</span><span class="sxs-lookup"><span data-stu-id="19392-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="19392-125">プログラムから、インデックスによって [LineAdjustFrom] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="19392-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19392-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="19392-126">Section index:</span></span>  <br/> |<span data-ttu-id="19392-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="19392-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="19392-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="19392-128">Row index:</span></span>  <br/> |<span data-ttu-id="19392-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="19392-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="19392-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="19392-130">Cell index:</span></span>  <br/> |<span data-ttu-id="19392-131">**visPLOLineAdjustFrom**</span><span class="sxs-lookup"><span data-stu-id="19392-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

