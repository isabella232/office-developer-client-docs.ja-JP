---
title: '[PageLineJumpDirY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: 図面ページ上にある垂直方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。
ms.openlocfilehash: 640ad93fbccf2cec26bda535c288c881aea32207
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805972"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a><span data-ttu-id="43254-103">[PageLineJumpDirY] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="43254-103">PageLineJumpDirY Cell (Page Layout Section)</span></span>

<span data-ttu-id="43254-104">図面ページ上にある垂直方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。</span><span class="sxs-lookup"><span data-stu-id="43254-104">Determines the direction of line jumps on vertical dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="43254-105">**値**</span><span class="sxs-lookup"><span data-stu-id="43254-105">**Value**</span></span>|<span data-ttu-id="43254-106">**線の飛び越し点の方向**</span><span class="sxs-lookup"><span data-stu-id="43254-106">**Line jump direction**</span></span>|<span data-ttu-id="43254-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="43254-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="43254-108">0</span><span class="sxs-lookup"><span data-stu-id="43254-108">0</span></span>  <br/> | <span data-ttu-id="43254-109">既定値です。上、またはページの設定に従います。</span><span class="sxs-lookup"><span data-stu-id="43254-109">Default; up or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="43254-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="43254-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="43254-111">1</span><span class="sxs-lookup"><span data-stu-id="43254-111">1</span></span>  <br/> | <span data-ttu-id="43254-112">左</span><span class="sxs-lookup"><span data-stu-id="43254-112">Left</span></span>  <br/> |<span data-ttu-id="43254-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="43254-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="43254-114">2</span><span class="sxs-lookup"><span data-stu-id="43254-114">2</span></span>  <br/> | <span data-ttu-id="43254-115">右</span><span class="sxs-lookup"><span data-stu-id="43254-115">Right</span></span>  <br/> |<span data-ttu-id="43254-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="43254-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43254-117">備考</span><span class="sxs-lookup"><span data-stu-id="43254-117">Remarks</span></span>

<span data-ttu-id="43254-118">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PageLineJumpDirY] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="43254-118">To get a reference to the PageLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="43254-119">セル名 :</span><span class="sxs-lookup"><span data-stu-id="43254-119">Cell name:</span></span>  <br/> | <span data-ttu-id="43254-120">PageLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="43254-120">PageLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="43254-121">プログラムから、インデックスによって [PageLineJumpDirY] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="43254-121">To get a reference to the PageLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="43254-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="43254-122">Section index:</span></span>  <br/> |<span data-ttu-id="43254-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="43254-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="43254-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="43254-124">Row index:</span></span>  <br/> |<span data-ttu-id="43254-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="43254-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="43254-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="43254-126">Cell index:</span></span>  <br/> |<span data-ttu-id="43254-127">**visPLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="43254-127">**visPLOJumpDirY**</span></span> <br/> |
   

