---
title: '[PlowCode] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: 図面ページで、配置可能な図形を別の配置可能な図形の近くにドロップしたときに、これらの図形を移動して遠ざけるかどうかを指定します。
ms.openlocfilehash: 4ea85ddbaf7662305a2a82fc7f0b814019624841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420354"
---
# <a name="plowcode-cell-page-layout-section"></a><span data-ttu-id="096d2-103">[PlowCode] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="096d2-103">PlowCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="096d2-104">図面ページで、配置可能な図形を別の配置可能な図形の近くにドロップしたときに、これらの図形を移動して遠ざけるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="096d2-104">Determines whether placeable shapes move away when you drop a placeable shape near another placeable shape on the drawing page.</span></span>
  
|<span data-ttu-id="096d2-105">**値**</span><span class="sxs-lookup"><span data-stu-id="096d2-105">**Value**</span></span>|<span data-ttu-id="096d2-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="096d2-106">**Description**</span></span>|<span data-ttu-id="096d2-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="096d2-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="096d2-108">0</span><span class="sxs-lookup"><span data-stu-id="096d2-108">0</span></span>  <br/> |<span data-ttu-id="096d2-109">図形を移動しません。</span><span class="sxs-lookup"><span data-stu-id="096d2-109">Don't move shapes</span></span>  <br/> |<span data-ttu-id="096d2-110">**visPLOPlowNone**</span><span class="sxs-lookup"><span data-stu-id="096d2-110">**visPLOPlowNone**</span></span> <br/> |
|<span data-ttu-id="096d2-111">1</span><span class="sxs-lookup"><span data-stu-id="096d2-111">1</span></span>  <br/> |<span data-ttu-id="096d2-112">図形を移動します。</span><span class="sxs-lookup"><span data-stu-id="096d2-112">Move shapes</span></span>  <br/> |<span data-ttu-id="096d2-113">**visPLOPlowAll**</span><span class="sxs-lookup"><span data-stu-id="096d2-113">**visPLOPlowAll**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="096d2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="096d2-114">Remarks</span></span>

<span data-ttu-id="096d2-115">[ページ設定] ダイアログ ボックスの [レイアウトとルーティング] タブ([デザイン] タブの [ページ設定] 矢印をクリック)で、[他の図形をドロップ時に移動] チェック ボックスを使用して、このセルの値を設定することもできます。  </span><span class="sxs-lookup"><span data-stu-id="096d2-115">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) by using the **Move other shapes away on drop** check box.</span></span> 
  
<span data-ttu-id="096d2-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PlowCode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="096d2-116">To get a reference to the PlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="096d2-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="096d2-117">Cell name:</span></span>  <br/> |<span data-ttu-id="096d2-118">PlowCode</span><span class="sxs-lookup"><span data-stu-id="096d2-118">PlowCode</span></span>  <br/> |
   
<span data-ttu-id="096d2-119">プログラムから、インデックスによって [PlowCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="096d2-119">To get a reference to the PlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="096d2-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="096d2-120">Section index:</span></span>  <br/> |<span data-ttu-id="096d2-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="096d2-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="096d2-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="096d2-122">Row index:</span></span>  <br/> |<span data-ttu-id="096d2-123">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="096d2-123">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="096d2-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="096d2-124">Cell index:</span></span>  <br/> |<span data-ttu-id="096d2-125">**visPLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="096d2-125">**visPLOPlowCode**</span></span> <br/> |
   

