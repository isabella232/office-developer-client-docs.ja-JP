---
title: '[Sharpen] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm910
localization_priority: Normal
ms.assetid: aa2bebfc-a6bb-a6b3-3ae9-8553f96b5738
description: ビットマップ イメージを鮮明にします。既定値は 0% です。イメージを鮮明にすると、隣接するピクセルのコントラストが上がり、イメージがはっきりと表示されます。
ms.openlocfilehash: e519cf6e5a168b64b4bc8aa083843163a47525ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415923"
---
# <a name="sharpen-cell-image-properties-section"></a><span data-ttu-id="32309-105">[Sharpen] セル ([Image Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="32309-105">Sharpen Cell (Image Properties Section)</span></span>

<span data-ttu-id="32309-p102">ビットマップ イメージを鮮明にします。既定値は 0% です。イメージを鮮明にすると、隣接するピクセルのコントラストが上がり、イメージがはっきりと表示されます。</span><span class="sxs-lookup"><span data-stu-id="32309-p102">Sharpens a bitmap image. The default value is 0%. Sharpening an image focuses it by increasing the contrast of adjacent pixels.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="32309-109">注釈</span><span class="sxs-lookup"><span data-stu-id="32309-109">Remarks</span></span>

<span data-ttu-id="32309-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Sharpen] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="32309-110">To get a reference to the Sharpen cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="32309-111">セル名 :</span><span class="sxs-lookup"><span data-stu-id="32309-111">Cell name:</span></span>  <br/> | <span data-ttu-id="32309-112">シャープ</span><span class="sxs-lookup"><span data-stu-id="32309-112">Sharpen</span></span>  <br/> |
   
<span data-ttu-id="32309-113">プログラムから、インデックスによって [Sharpen] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="32309-113">To get a reference to the Sharpen cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="32309-114">セクション インデックス :</span><span class="sxs-lookup"><span data-stu-id="32309-114">Section index:</span></span>  <br/> |<span data-ttu-id="32309-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="32309-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="32309-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="32309-116">Row index:</span></span>  <br/> |<span data-ttu-id="32309-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="32309-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="32309-118">セル インデックス :</span><span class="sxs-lookup"><span data-stu-id="32309-118">Cell index:</span></span>  <br/> |<span data-ttu-id="32309-119">**visImageSharpen**</span><span class="sxs-lookup"><span data-stu-id="32309-119">**visImageSharpen**</span></span> <br/> |
   

