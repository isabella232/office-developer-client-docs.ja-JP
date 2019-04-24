---
title: '[ImgOffsetY] セル ([Foreign Image Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm455
localization_priority: Normal
ms.assetid: 3b2991aa-4722-fe3b-39c5-02d38c4c7efc
description: オブジェクトの枠の原点からオブジェクトを垂直方向へオフセットする距離を指定します。 既定値は 0 です。 [トリミング ツール] を使用してオブジェクトをパンすると、この値が変化します。
ms.openlocfilehash: 908972216a24370bc48990ddc99a36da9274d648
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344738"
---
# <a name="imgoffsety-cell-foreign-image-info-section"></a><span data-ttu-id="089c5-105">[ImgOffsetY] セル ([Foreign Image Info] セクション)</span><span class="sxs-lookup"><span data-stu-id="089c5-105">ImgOffsetY Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="089c5-p102">オブジェクトの枠の原点からオブジェクトを垂直方向へオフセットする距離を指定します。既定値は 0 です。**[トリミング ツール]** を使用してオブジェクトをパンすると、この値が変化します。</span><span class="sxs-lookup"><span data-stu-id="089c5-p102">Determines the distance the object is offset vertically from the origin of the object's border. The default is 0. Panning the object with the **Crop** tool changes this value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="089c5-109">解説</span><span class="sxs-lookup"><span data-stu-id="089c5-109">Remarks</span></span>

<span data-ttu-id="089c5-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ImgOffsetY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="089c5-110">To get a reference to the ImgOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="089c5-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="089c5-111">Cell name:</span></span>  <br/> | <span data-ttu-id="089c5-112">[imgoffsety]</span><span class="sxs-lookup"><span data-stu-id="089c5-112">ImgOffsetY</span></span>  <br/> |
   
<span data-ttu-id="089c5-113">プログラムから、インデックスによって [ImgOffsetY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="089c5-113">To get a reference to the ImgOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="089c5-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="089c5-114">Section index:</span></span>  <br/> |<span data-ttu-id="089c5-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="089c5-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="089c5-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="089c5-116">Row index:</span></span>  <br/> |<span data-ttu-id="089c5-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="089c5-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="089c5-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="089c5-118">Cell index:</span></span>  <br/> |<span data-ttu-id="089c5-119">**visFrgnImgOffsetY**</span><span class="sxs-lookup"><span data-stu-id="089c5-119">**visFrgnImgOffsetY**</span></span> <br/> |
   

