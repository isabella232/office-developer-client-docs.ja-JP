---
title: '[Brightness] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251608
localization_priority: Normal
ms.assetid: 5bb1cc81-f3fd-a835-1449-233dbd1a62b6
description: ビットマップ イメージの明るさを調整します。0 ～ 49% の範囲で値を入力するとイメージの輝度が下がります。51 ～ 100% の範囲で値を入力するとイメージの輝度が上がります。既定値は 50% です。
ms.openlocfilehash: ae1390d2db3adad86a8afcbeaff88172a841d030
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424792"
---
# <a name="brightness-cell-image-properties-section"></a><span data-ttu-id="e83db-105">[Brightness] セル ([Image Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="e83db-105">Brightness Cell (Image Properties Section)</span></span>

<span data-ttu-id="e83db-p102">ビットマップ イメージの明るさを調整します。0 ～ 49% の範囲で値を入力するとイメージの輝度が下がります。51 ～ 100% の範囲で値を入力するとイメージの輝度が上がります。既定値は 50% です。</span><span class="sxs-lookup"><span data-stu-id="e83db-p102">Adjusts the brightness of a bitmap image. Decrease brightness of an image by entering a value between 0% and 49%, or increase brightness by entering a value between 51% and 100%. The default value is 50%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e83db-109">注釈</span><span class="sxs-lookup"><span data-stu-id="e83db-109">Remarks</span></span>

<span data-ttu-id="e83db-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Brightness] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e83db-110">To get a reference to the Brightness cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e83db-111">セル名 :</span><span class="sxs-lookup"><span data-stu-id="e83db-111">Cell name:</span></span>  <br/> | <span data-ttu-id="e83db-112">Brightness</span><span class="sxs-lookup"><span data-stu-id="e83db-112">Brightness</span></span>  <br/> |
   
<span data-ttu-id="e83db-113">プログラムから、インデックスによって [Brightness] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e83db-113">To get a reference to the Brightness cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e83db-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e83db-114">Section index:</span></span>  <br/> |<span data-ttu-id="e83db-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e83db-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e83db-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e83db-116">Row index:</span></span>  <br/> |<span data-ttu-id="e83db-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="e83db-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="e83db-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e83db-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e83db-119">**viシム age輝度**</span><span class="sxs-lookup"><span data-stu-id="e83db-119">**visImageBrightness**</span></span> <br/> |
   

