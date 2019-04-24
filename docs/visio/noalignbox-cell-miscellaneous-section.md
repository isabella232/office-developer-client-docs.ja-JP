---
title: '[NoAlignBox] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm700
localization_priority: Normal
ms.assetid: b2d51f4b-d64e-fd14-4ff1-ed67c69213bc
description: 選択した図形の選択範囲の表示/非表示を切り替えます。
ms.openlocfilehash: 2ff9f051df54f4d424589332b9fbaea973552edc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319860"
---
# <a name="noalignbox-cell-miscellaneous-section"></a><span data-ttu-id="6d11a-103">[NoAlignBox] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="6d11a-103">NoAlignBox Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="6d11a-104">選択した図形の選択範囲の表示/非表示を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="6d11a-104">Switches the display of the selection rectangle on and off for the selected shape.</span></span>
  
|<span data-ttu-id="6d11a-105">**値**</span><span class="sxs-lookup"><span data-stu-id="6d11a-105">**Value**</span></span>|<span data-ttu-id="6d11a-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="6d11a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6d11a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="6d11a-107">TRUE</span></span>  <br/> | <span data-ttu-id="6d11a-108">図形を選択するときに選択範囲が表示されません。</span><span class="sxs-lookup"><span data-stu-id="6d11a-108">Selection rectangle is not displayed when the shape is selected.</span></span>  <br/> |
| <span data-ttu-id="6d11a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="6d11a-109">FALSE</span></span>  <br/> | <span data-ttu-id="6d11a-110">図形を選択するときに選択範囲が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6d11a-110">Selection rectangle is displayed when the shape is selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d11a-111">解説</span><span class="sxs-lookup"><span data-stu-id="6d11a-111">Remarks</span></span>

<span data-ttu-id="6d11a-112">別の数式または **CellsU** を使用したプログラムから、名前によって [NoAlignBox] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-112">To get a reference to the NoAlignBox cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d11a-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="6d11a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="6d11a-114">[noalignbox]</span><span class="sxs-lookup"><span data-stu-id="6d11a-114">NoAlignBox</span></span>  <br/> |
   
<span data-ttu-id="6d11a-115">プログラムから、インデックスによって [NoAlignBox] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-115">To get a reference to the NoAlignBox cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d11a-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6d11a-116">Section index:</span></span>  <br/> |<span data-ttu-id="6d11a-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6d11a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6d11a-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6d11a-118">Row index:</span></span>  <br/> |<span data-ttu-id="6d11a-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="6d11a-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="6d11a-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6d11a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="6d11a-121">**visNoAlignBox**</span><span class="sxs-lookup"><span data-stu-id="6d11a-121">**visNoAlignBox**</span></span> <br/> |
   

