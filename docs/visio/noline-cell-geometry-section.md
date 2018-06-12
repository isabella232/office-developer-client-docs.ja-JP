---
title: '[NoLine] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: パスの境界に線を描画するかどうかを指定します。
ms.openlocfilehash: 1e43072363461e6b8fcd511c70512f3bfef4504f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805918"
---
# <a name="noline-cell-geometry-section"></a><span data-ttu-id="a24df-103">[NoLine] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="a24df-103">NoLine Cell (Geometry Section)</span></span>

<span data-ttu-id="a24df-104">パスの境界に線を描画するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a24df-104">Determines whether a line is drawn around the boundary of the path.</span></span>
  
|<span data-ttu-id="a24df-105">**値**</span><span class="sxs-lookup"><span data-stu-id="a24df-105">**Value**</span></span>|<span data-ttu-id="a24df-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="a24df-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a24df-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a24df-107">TRUE</span></span>  <br/> | <span data-ttu-id="a24df-108">塗りつぶし領域の境界になっているパスの境界に線を描画しません。</span><span class="sxs-lookup"><span data-stu-id="a24df-108">A line is not drawn around the boundary of the path that is the boundary of a filled region.</span></span>  <br/> |
| <span data-ttu-id="a24df-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a24df-109">FALSE</span></span>  <br/> | <span data-ttu-id="a24df-110">パスの境界に線を描画します。</span><span class="sxs-lookup"><span data-stu-id="a24df-110">A line is drawn around the boundary of a path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a24df-111">備考</span><span class="sxs-lookup"><span data-stu-id="a24df-111">Remarks</span></span>

<span data-ttu-id="a24df-p101">線の色を白に変更すると、白い背景では見えなくなりますが、線は存在しています。このセルの値を TRUE に設定すると、線は描画されません。</span><span class="sxs-lookup"><span data-stu-id="a24df-p101">When you change the color of a line to white, the line still exists even though you can't see it on a white background. When you set the value of this cell to TRUE, no line is drawn.</span></span>
  
<span data-ttu-id="a24df-114">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [noline] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="a24df-114">To get a reference to the NoLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a24df-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="a24df-115">Cell name:</span></span>  <br/> | <span data-ttu-id="a24df-116">ジオメトリの*i*です。[Noline]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="a24df-116">Geometry  *i*  .NoLine            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a24df-117">プログラムから、インデックスによって [noline] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a24df-117">To get a reference to the NoLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a24df-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a24df-118">Section index:</span></span>  <br/> |<span data-ttu-id="a24df-119">**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="a24df-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a24df-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a24df-120">Row index:</span></span>  <br/> |<span data-ttu-id="a24df-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="a24df-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="a24df-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a24df-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a24df-123">**visCompNoLine**</span><span class="sxs-lookup"><span data-stu-id="a24df-123">**visCompNoLine**</span></span> <br/> |
   

