---
title: '[NoShow] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: 図面ページにパスを表示するかどうかを示します。
ms.openlocfilehash: bd42b069e6796b107aafaea3080f6970c4f678c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341084"
---
# <a name="noshow-cell-geometry-section"></a><span data-ttu-id="bceb4-103">[NoShow] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="bceb4-103">NoShow Cell (Geometry Section)</span></span>

<span data-ttu-id="bceb4-104">図面ページにパスを表示するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bceb4-104">Indicates whether a path is displayed on the drawing page.</span></span>
  
|<span data-ttu-id="bceb4-105">**値**</span><span class="sxs-lookup"><span data-stu-id="bceb4-105">**Value**</span></span>|<span data-ttu-id="bceb4-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="bceb4-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bceb4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bceb4-107">TRUE</span></span>  <br/> | <span data-ttu-id="bceb4-108">図形座標セクションによって描画されるパスのストロークと塗りつぶしは表示されません。</span><span class="sxs-lookup"><span data-stu-id="bceb4-108">The stroke and fill of the path represented by the section is hidden.</span></span>  <br/> |
| <span data-ttu-id="bceb4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bceb4-109">FALSE</span></span>  <br/> | <span data-ttu-id="bceb4-110">パスのストロークと塗りつぶしは表示されます。</span><span class="sxs-lookup"><span data-stu-id="bceb4-110">The stroke and fill of the path is shown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bceb4-111">解説</span><span class="sxs-lookup"><span data-stu-id="bceb4-111">Remarks</span></span>

<span data-ttu-id="bceb4-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoShow] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bceb4-112">To get a reference to the NoShow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bceb4-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="bceb4-113">Cell name:</span></span>  <br/> | <span data-ttu-id="bceb4-114">ジオメトリ*i*[noshow] where *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="bceb4-114">Geometry  *i*  .NoShow            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bceb4-115">プログラムから、インデックスによって [NoShow] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bceb4-115">To get a reference to the NoShow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bceb4-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bceb4-116">Section index:</span></span>  <br/> |<span data-ttu-id="bceb4-117">**visSectionFirstComponent** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="bceb4-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bceb4-118">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="bceb4-118">Row index:</span></span>  <br/> |<span data-ttu-id="bceb4-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="bceb4-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="bceb4-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bceb4-120">Cell index:</span></span>  <br/> |<span data-ttu-id="bceb4-121">**visCompNoShow**</span><span class="sxs-lookup"><span data-stu-id="bceb4-121">**visCompNoShow**</span></span> <br/> |
   

