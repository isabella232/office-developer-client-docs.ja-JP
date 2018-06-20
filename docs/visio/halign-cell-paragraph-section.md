---
title: '[HAlign] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: 図形のテキスト ブロックにあるテキストの水平方向の配置を指定します。
ms.openlocfilehash: 224e495e8aea70c418a0ab7f5a7d56975d9868e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805516"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="05bb8-103">[HAlign] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="05bb8-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="05bb8-104">図形のテキスト ブロックにあるテキストの水平方向の配置を指定します。</span><span class="sxs-lookup"><span data-stu-id="05bb8-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="05bb8-105">**値**</span><span class="sxs-lookup"><span data-stu-id="05bb8-105">**Value**</span></span>|<span data-ttu-id="05bb8-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="05bb8-106">**Description**</span></span>|<span data-ttu-id="05bb8-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="05bb8-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="05bb8-108">0</span><span class="sxs-lookup"><span data-stu-id="05bb8-108">0</span></span>  <br/> | <span data-ttu-id="05bb8-109">左揃え</span><span class="sxs-lookup"><span data-stu-id="05bb8-109">Left align</span></span>  <br/> |<span data-ttu-id="05bb8-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="05bb8-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="05bb8-111">1</span><span class="sxs-lookup"><span data-stu-id="05bb8-111">1</span></span>  <br/> | <span data-ttu-id="05bb8-112">中央揃え</span><span class="sxs-lookup"><span data-stu-id="05bb8-112">Center</span></span>  <br/> |<span data-ttu-id="05bb8-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="05bb8-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="05bb8-114">2</span><span class="sxs-lookup"><span data-stu-id="05bb8-114">2</span></span>  <br/> | <span data-ttu-id="05bb8-115">右揃え</span><span class="sxs-lookup"><span data-stu-id="05bb8-115">Right align</span></span>  <br/> |<span data-ttu-id="05bb8-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="05bb8-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="05bb8-117">3</span><span class="sxs-lookup"><span data-stu-id="05bb8-117">3</span></span>  <br/> | <span data-ttu-id="05bb8-118">両端揃え</span><span class="sxs-lookup"><span data-stu-id="05bb8-118">Justify</span></span>  <br/> |<span data-ttu-id="05bb8-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="05bb8-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="05bb8-120">4</span><span class="sxs-lookup"><span data-stu-id="05bb8-120">4</span></span>  <br/> | <span data-ttu-id="05bb8-121">均等割付</span><span class="sxs-lookup"><span data-stu-id="05bb8-121">Force justify</span></span>  <br/> |<span data-ttu-id="05bb8-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="05bb8-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05bb8-123">備考</span><span class="sxs-lookup"><span data-stu-id="05bb8-123">Remarks</span></span>

<span data-ttu-id="05bb8-124">両端揃えの場合、段落の最終行以外の各行の単語間に空白が挿入されて、テキストの左右の両端が余白に合わせて揃えられます</span><span class="sxs-lookup"><span data-stu-id="05bb8-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="05bb8-125">均等割付の場合は、段落の最終行も含めて、すべての行の両端を揃えます。</span><span class="sxs-lookup"><span data-stu-id="05bb8-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="05bb8-126">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [halign] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="05bb8-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05bb8-127">セル名:</span><span class="sxs-lookup"><span data-stu-id="05bb8-127">Cell name:</span></span>  <br/> | <span data-ttu-id="05bb8-128">Para.HorzAlign [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="05bb8-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="05bb8-129">プログラムから、インデックスによって [halign] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="05bb8-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05bb8-130">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="05bb8-130">Section index:</span></span>  <br/> |<span data-ttu-id="05bb8-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="05bb8-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="05bb8-132">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="05bb8-132">Row index:</span></span>  <br/> |<span data-ttu-id="05bb8-133">**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="05bb8-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="05bb8-134">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="05bb8-134">Cell index:</span></span>  <br/> |<span data-ttu-id="05bb8-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="05bb8-135">**visHorzAlign**</span></span> <br/> |
   

