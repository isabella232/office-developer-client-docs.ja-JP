---
title: '[NoFill] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: パスに塗りつぶしを適用するかどうかを指定します。
ms.openlocfilehash: 301f30b644e338ff9e597a7a7d8226b9c8a4462f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415020"
---
# <a name="nofill-cell-geometry-section"></a><span data-ttu-id="0e708-103">[NoFill] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="0e708-103">NoFill Cell (Geometry Section)</span></span>

<span data-ttu-id="0e708-104">パスに塗りつぶしを適用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="0e708-104">Indicates whether a path can be filled.</span></span>
  
|<span data-ttu-id="0e708-105">**値**</span><span class="sxs-lookup"><span data-stu-id="0e708-105">**Value**</span></span>|<span data-ttu-id="0e708-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="0e708-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0e708-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0e708-107">TRUE</span></span>  <br/> | <span data-ttu-id="0e708-108">図形の他のパスが塗りつぶされていても、このパスは塗りつぶされません。</span><span class="sxs-lookup"><span data-stu-id="0e708-108">The path is not filled even if other paths in the shape are filled.</span></span>  <br/> |
| <span data-ttu-id="0e708-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0e708-109">FALSE</span></span>  <br/> | <span data-ttu-id="0e708-110">パスが閉じていない場合でも、図形の塗りつぶしがこのパスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="0e708-110">The shape's fill applies to the path, even if it isn't closed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e708-111">注釈</span><span class="sxs-lookup"><span data-stu-id="0e708-111">Remarks</span></span>

<span data-ttu-id="0e708-p101">図形の塗りつぶしパターンをゼロ (0) に設定すると、すべてのパスに対して塗りつぶしが適用されません。図形内にある特定のパスに対して塗りつぶしを適用しない場合に、このセルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0e708-p101">If you set a shape's fill pattern to none (0), none of its paths are filled. This cell is used to turn the fill off selectively for a path within a shape.</span></span>
  
<span data-ttu-id="0e708-114">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoFill] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e708-114">To get a reference to the NoFill cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e708-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="0e708-115">Cell name:</span></span>  <br/> | <span data-ttu-id="0e708-116">ジオメトリ*i*[nofill] where *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="0e708-116">Geometry  *i*  .NoFill            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0e708-117">プログラムから、インデックスによって [NoFill] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0e708-117">To get a reference to the NoFill cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e708-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0e708-118">Section index:</span></span>  <br/> |<span data-ttu-id="0e708-119">**visSectionFirstComponent** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="0e708-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0e708-120">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="0e708-120">Row index:</span></span>  <br/> |<span data-ttu-id="0e708-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="0e708-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="0e708-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0e708-122">Cell index:</span></span>  <br/> |<span data-ttu-id="0e708-123">**visCompNoFill**</span><span class="sxs-lookup"><span data-stu-id="0e708-123">**visCompNoFill**</span></span> <br/> |
   

