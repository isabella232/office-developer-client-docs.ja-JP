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
ms.openlocfilehash: ad4d9cf1aa3e541f512bc09ffc38cf03204b3c94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805957"
---
# <a name="noshow-cell-geometry-section"></a><span data-ttu-id="f0b07-103">[NoShow] セル ([Geometry] セクション)</span><span class="sxs-lookup"><span data-stu-id="f0b07-103">NoShow Cell (Geometry Section)</span></span>

<span data-ttu-id="f0b07-104">図面ページにパスを表示するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f0b07-104">Indicates whether a path is displayed on the drawing page.</span></span>
  
|<span data-ttu-id="f0b07-105">**値**</span><span class="sxs-lookup"><span data-stu-id="f0b07-105">**Value**</span></span>|<span data-ttu-id="f0b07-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="f0b07-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f0b07-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f0b07-107">TRUE</span></span>  <br/> | <span data-ttu-id="f0b07-108">図形座標セクションによって描画されるパスのストロークと塗りつぶしは表示されません。</span><span class="sxs-lookup"><span data-stu-id="f0b07-108">The stroke and fill of the path represented by the section is hidden.</span></span>  <br/> |
| <span data-ttu-id="f0b07-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f0b07-109">FALSE</span></span>  <br/> | <span data-ttu-id="f0b07-110">パスのストロークと塗りつぶしは表示されます。</span><span class="sxs-lookup"><span data-stu-id="f0b07-110">The stroke and fill of the path is shown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0b07-111">備考</span><span class="sxs-lookup"><span data-stu-id="f0b07-111">Remarks</span></span>

<span data-ttu-id="f0b07-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [noshow] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="f0b07-112">To get a reference to the NoShow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0b07-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="f0b07-113">Cell name:</span></span>  <br/> | <span data-ttu-id="f0b07-114">ジオメトリの*i*です。[Noshow]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="f0b07-114">Geometry  *i*  .NoShow            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f0b07-115">プログラムから、インデックスによって [noshow] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="f0b07-115">To get a reference to the NoShow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0b07-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f0b07-116">Section index:</span></span>  <br/> |<span data-ttu-id="f0b07-117">**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="f0b07-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f0b07-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f0b07-118">Row index:</span></span>  <br/> |<span data-ttu-id="f0b07-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="f0b07-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="f0b07-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f0b07-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f0b07-121">**visCompNoShow**</span><span class="sxs-lookup"><span data-stu-id="f0b07-121">**visCompNoShow**</span></span> <br/> |
   

