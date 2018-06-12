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
ms.openlocfilehash: 688a6cacfa9100ad116b9bf06926194c24712219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804917"
---
# <a name="brightness-cell-image-properties-section"></a><span data-ttu-id="875cd-105">[Brightness] セル ([Image Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="875cd-105">Brightness Cell (Image Properties Section)</span></span>

<span data-ttu-id="875cd-p102">ビットマップ イメージの明るさを調整します。0 ～ 49% の範囲で値を入力するとイメージの輝度が下がります。51 ～ 100% の範囲で値を入力するとイメージの輝度が上がります。既定値は 50% です。</span><span class="sxs-lookup"><span data-stu-id="875cd-p102">Adjusts the brightness of a bitmap image. Decrease brightness of an image by entering a value between 0% and 49%, or increase brightness by entering a value between 51% and 100%. The default value is 50%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="875cd-109">備考</span><span class="sxs-lookup"><span data-stu-id="875cd-109">Remarks</span></span>

<span data-ttu-id="875cd-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[明るさ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="875cd-110">To get a reference to the Brightness cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="875cd-111">セル名 :</span><span class="sxs-lookup"><span data-stu-id="875cd-111">Cell name:</span></span>  <br/> | <span data-ttu-id="875cd-112">Brightness</span><span class="sxs-lookup"><span data-stu-id="875cd-112">Brightness</span></span>  <br/> |
   
<span data-ttu-id="875cd-113">プログラムから、インデックスによって [明るさ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="875cd-113">To get a reference to the Brightness cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="875cd-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="875cd-114">Section index:</span></span>  <br/> |<span data-ttu-id="875cd-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="875cd-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="875cd-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="875cd-116">Row index:</span></span>  <br/> |<span data-ttu-id="875cd-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="875cd-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="875cd-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="875cd-118">Cell index:</span></span>  <br/> |<span data-ttu-id="875cd-119">**visImageBrightness**</span><span class="sxs-lookup"><span data-stu-id="875cd-119">**visImageBrightness**</span></span> <br/> |
   
