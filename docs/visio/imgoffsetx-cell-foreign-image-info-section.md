---
title: '[ImgOffsetX] セル ([Foreign Image Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251308
localization_priority: Normal
ms.assetid: c079fb10-4db7-4657-75d2-2fb953c86670
description: オブジェクトの枠の原点からオブジェクトを水平方向へオフセットする距離を指定します。 既定値は 0 です。 [トリミング ツール] を使用してオブジェクトをパンすると、この値が変化します。
ms.openlocfilehash: d9b3e97a07bc1cadc0276905c4199861ab0590ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335407"
---
# <a name="imgoffsetx-cell-foreign-image-info-section"></a><span data-ttu-id="b1c17-105">[ImgOffsetX] セル ([Foreign Image Info] セクション)</span><span class="sxs-lookup"><span data-stu-id="b1c17-105">ImgOffsetX Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="b1c17-p102">オブジェクトの枠の原点からオブジェクトを水平方向へオフセットする距離を指定します。既定値は 0 です。**[トリミング ツール]** を使用してオブジェクトをパンすると、この値が変化します。</span><span class="sxs-lookup"><span data-stu-id="b1c17-p102">Determines the distance the object is offset horizontally from the origin of the object's border. The default is 0. Panning the object with the **Crop** tool changes this value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b1c17-109">解説</span><span class="sxs-lookup"><span data-stu-id="b1c17-109">Remarks</span></span>

<span data-ttu-id="b1c17-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ImgOffsetX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b1c17-110">To get a reference to the ImgOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1c17-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="b1c17-111">Cell name:</span></span>  <br/> | <span data-ttu-id="b1c17-112">[imgoffsetx]</span><span class="sxs-lookup"><span data-stu-id="b1c17-112">ImgOffsetX</span></span>  <br/> |
   
<span data-ttu-id="b1c17-113">プログラムから、インデックスによって [ImgOffsetX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1c17-113">To get a reference to the ImgOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1c17-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1c17-114">Section index:</span></span>  <br/> |<span data-ttu-id="b1c17-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b1c17-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b1c17-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1c17-116">Row index:</span></span>  <br/> |<span data-ttu-id="b1c17-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="b1c17-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="b1c17-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b1c17-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b1c17-119">**visFrgnImgOffsetX**</span><span class="sxs-lookup"><span data-stu-id="b1c17-119">**visFrgnImgOffsetX**</span></span> <br/> |
   

