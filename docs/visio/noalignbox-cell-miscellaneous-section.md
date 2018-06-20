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
ms.openlocfilehash: c8e5fe28197a72b4cdb5306732dd155dc8f4f810
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805916"
---
# <a name="noalignbox-cell-miscellaneous-section"></a><span data-ttu-id="a1d73-103">[NoAlignBox] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="a1d73-103">NoAlignBox Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="a1d73-104">選択した図形の選択範囲の表示/非表示を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="a1d73-104">Switches the display of the selection rectangle on and off for the selected shape.</span></span>
  
|<span data-ttu-id="a1d73-105">**値**</span><span class="sxs-lookup"><span data-stu-id="a1d73-105">**Value**</span></span>|<span data-ttu-id="a1d73-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="a1d73-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a1d73-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a1d73-107">TRUE</span></span>  <br/> | <span data-ttu-id="a1d73-108">図形を選択するときに選択範囲が表示されません。</span><span class="sxs-lookup"><span data-stu-id="a1d73-108">Selection rectangle is not displayed when the shape is selected.</span></span>  <br/> |
| <span data-ttu-id="a1d73-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a1d73-109">FALSE</span></span>  <br/> | <span data-ttu-id="a1d73-110">図形を選択するときに選択範囲が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a1d73-110">Selection rectangle is displayed when the shape is selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1d73-111">備考</span><span class="sxs-lookup"><span data-stu-id="a1d73-111">Remarks</span></span>

<span data-ttu-id="a1d73-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[NoAlignBox] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="a1d73-112">To get a reference to the NoAlignBox cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a1d73-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="a1d73-113">Cell name:</span></span>  <br/> | <span data-ttu-id="a1d73-114">NoAlignBox</span><span class="sxs-lookup"><span data-stu-id="a1d73-114">NoAlignBox</span></span>  <br/> |
   
<span data-ttu-id="a1d73-115">プログラムから、インデックスによって [NoAlignBox] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a1d73-115">To get a reference to the NoAlignBox cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a1d73-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a1d73-116">Section index:</span></span>  <br/> |<span data-ttu-id="a1d73-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a1d73-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a1d73-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a1d73-118">Row index:</span></span>  <br/> |<span data-ttu-id="a1d73-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="a1d73-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="a1d73-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a1d73-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a1d73-121">**visNoAlignBox**</span><span class="sxs-lookup"><span data-stu-id="a1d73-121">**visNoAlignBox**</span></span> <br/> |
   

