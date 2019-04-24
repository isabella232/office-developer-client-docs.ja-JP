---
title: '[ImgWidth] セル ([Foreign Image Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 枠内におけるオブジェクトのイメージの幅を指定します。 既定の数式は次のとおりです。
ms.openlocfilehash: 9da5e06a7fbf6ae77a49fb0410aefb406e2afecb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344724"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a><span data-ttu-id="e1ba2-104">[ImgWidth] セル ([Foreign Image Info] セクション)</span><span class="sxs-lookup"><span data-stu-id="e1ba2-104">ImgWidth Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="e1ba2-105">枠内におけるオブジェクトのイメージの幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-105">Determines the width of the object's image within its border.</span></span> <span data-ttu-id="e1ba2-106">既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-106">The default formula is:</span></span>
  
<span data-ttu-id="e1ba2-107">= 幅\* 1</span><span class="sxs-lookup"><span data-stu-id="e1ba2-107">= Width \* 1</span></span>
  
<span data-ttu-id="e1ba2-108">オブジェクトをトリミングすると、Width に掛ける係数が変化します。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-108">Cropping the object changes the factor by which Width is multiplied.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e1ba2-109">解説</span><span class="sxs-lookup"><span data-stu-id="e1ba2-109">Remarks</span></span>

<span data-ttu-id="e1ba2-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ImgWidth] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-110">To get a reference to the ImgWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e1ba2-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="e1ba2-111">Cell name:</span></span>  <br/> | <span data-ttu-id="e1ba2-112">[imgwidth]</span><span class="sxs-lookup"><span data-stu-id="e1ba2-112">ImgWidth</span></span>  <br/> |
   
<span data-ttu-id="e1ba2-113">プログラムから、インデックスによって [ImgWidth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e1ba2-113">To get a reference to the ImgWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e1ba2-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e1ba2-114">Section index:</span></span>  <br/> |<span data-ttu-id="e1ba2-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e1ba2-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e1ba2-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e1ba2-116">Row index:</span></span>  <br/> |<span data-ttu-id="e1ba2-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="e1ba2-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="e1ba2-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e1ba2-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e1ba2-119">**visFrgnImgWidth**</span><span class="sxs-lookup"><span data-stu-id="e1ba2-119">**visFrgnImgWidth**</span></span> <br/> |
   

