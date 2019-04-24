---
title: '[Contrast] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm200
localization_priority: Normal
ms.assetid: f0e4c644-c646-9649-c697-82feb02f5e29
description: ビットマップ イメージのコントラストを調整します。0 ～ 49% の範囲で値を入力するとイメージのコントラストが下がります。51 ～ 100% の範囲で値を入力するとイメージのコントラストが上がります。既定値は 50% です。
ms.openlocfilehash: f0a27090ea1ec96bf11726ae641ff918dd581e2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319021"
---
# <a name="contrast-cell-image-properties-section"></a><span data-ttu-id="691fb-105">[Contrast] セル ([Image Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="691fb-105">Contrast Cell (Image Properties Section)</span></span>

<span data-ttu-id="691fb-p102">ビットマップ イメージのコントラストを調整します。0 ～ 49% の範囲で値を入力するとイメージのコントラストが下がります。51 ～ 100% の範囲で値を入力するとイメージのコントラストが上がります。既定値は 50% です。</span><span class="sxs-lookup"><span data-stu-id="691fb-p102">Adjusts the contrast of a bitmap image. Decrease the contrast of an image by entering a value between 0% and 49%, or increase the contrast by entering a value between 51% and 100%. The default value is 50%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="691fb-109">解説</span><span class="sxs-lookup"><span data-stu-id="691fb-109">Remarks</span></span>

<span data-ttu-id="691fb-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Contrast] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="691fb-110">To get a reference to the Contrast cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="691fb-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="691fb-111">Cell name:</span></span>  <br/> | <span data-ttu-id="691fb-112">Contrast</span><span class="sxs-lookup"><span data-stu-id="691fb-112">Contrast</span></span>  <br/> |
   
<span data-ttu-id="691fb-113">プログラムから、インデックスによって [Contrast] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="691fb-113">To get a reference to the Contrast cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="691fb-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="691fb-114">Section index:</span></span>  <br/> |<span data-ttu-id="691fb-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="691fb-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="691fb-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="691fb-116">Row index:</span></span>  <br/> |<span data-ttu-id="691fb-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="691fb-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="691fb-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="691fb-118">Cell index:</span></span>  <br/> |<span data-ttu-id="691fb-119">**visimagecontrast**</span><span class="sxs-lookup"><span data-stu-id="691fb-119">**visImageContrast**</span></span> <br/> |
   

