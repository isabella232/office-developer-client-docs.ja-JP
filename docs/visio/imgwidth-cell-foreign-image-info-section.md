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
description: 枠内におけるオブジェクトのイメージの幅を指定します。既定の数式は次のとおりです。
ms.openlocfilehash: 3aab65d27d426287060f7572dad15174acb93199
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805572"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a><span data-ttu-id="77465-104">[ImgWidth] セル ([Foreign Image Info] セクション)</span><span class="sxs-lookup"><span data-stu-id="77465-104">ImgWidth Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="77465-p102">枠内におけるオブジェクトのイメージの幅を指定します。既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="77465-p102">Determines the width of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="77465-107">= 幅\*1</span><span class="sxs-lookup"><span data-stu-id="77465-107">= Width \* 1</span></span>
  
<span data-ttu-id="77465-108">オブジェクトをトリミングすると、Width に掛ける係数が変化します。</span><span class="sxs-lookup"><span data-stu-id="77465-108">Cropping the object changes the factor by which Width is multiplied.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="77465-109">備考</span><span class="sxs-lookup"><span data-stu-id="77465-109">Remarks</span></span>

<span data-ttu-id="77465-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [imgwidth] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="77465-110">To get a reference to the ImgWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="77465-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="77465-111">Cell name:</span></span>  <br/> | <span data-ttu-id="77465-112">[Imgwidth]</span><span class="sxs-lookup"><span data-stu-id="77465-112">ImgWidth</span></span>  <br/> |
   
<span data-ttu-id="77465-113">プログラムから、インデックスによって [imgwidth] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="77465-113">To get a reference to the ImgWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="77465-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="77465-114">Section index:</span></span>  <br/> |<span data-ttu-id="77465-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="77465-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="77465-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="77465-116">Row index:</span></span>  <br/> |<span data-ttu-id="77465-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="77465-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="77465-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="77465-118">Cell index:</span></span>  <br/> |<span data-ttu-id="77465-119">**visFrgnImgWidth**</span><span class="sxs-lookup"><span data-stu-id="77465-119">**visFrgnImgWidth**</span></span> <br/> |
   

