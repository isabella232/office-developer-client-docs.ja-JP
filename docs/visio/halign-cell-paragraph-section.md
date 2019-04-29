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
ms.openlocfilehash: a48619e2531c0a69ad63af3b88ae9f019019b1fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414740"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="7a76c-103">[HAlign] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="7a76c-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="7a76c-104">図形のテキスト ブロックにあるテキストの水平方向の配置を指定します。</span><span class="sxs-lookup"><span data-stu-id="7a76c-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="7a76c-105">**値**</span><span class="sxs-lookup"><span data-stu-id="7a76c-105">**Value**</span></span>|<span data-ttu-id="7a76c-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="7a76c-106">**Description**</span></span>|<span data-ttu-id="7a76c-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="7a76c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7a76c-108">.0</span><span class="sxs-lookup"><span data-stu-id="7a76c-108">0</span></span>  <br/> | <span data-ttu-id="7a76c-109">左揃え</span><span class="sxs-lookup"><span data-stu-id="7a76c-109">Left align</span></span>  <br/> |<span data-ttu-id="7a76c-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="7a76c-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="7a76c-111">1 </span><span class="sxs-lookup"><span data-stu-id="7a76c-111">1</span></span>  <br/> | <span data-ttu-id="7a76c-112">中央</span><span class="sxs-lookup"><span data-stu-id="7a76c-112">Center</span></span>  <br/> |<span data-ttu-id="7a76c-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="7a76c-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="7a76c-114">2 </span><span class="sxs-lookup"><span data-stu-id="7a76c-114">2</span></span>  <br/> | <span data-ttu-id="7a76c-115">右揃え</span><span class="sxs-lookup"><span data-stu-id="7a76c-115">Right align</span></span>  <br/> |<span data-ttu-id="7a76c-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="7a76c-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="7a76c-117">3 </span><span class="sxs-lookup"><span data-stu-id="7a76c-117">3</span></span>  <br/> | <span data-ttu-id="7a76c-118">Justify</span><span class="sxs-lookup"><span data-stu-id="7a76c-118">Justify</span></span>  <br/> |<span data-ttu-id="7a76c-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="7a76c-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="7a76c-120">4 </span><span class="sxs-lookup"><span data-stu-id="7a76c-120">4</span></span>  <br/> | <span data-ttu-id="7a76c-121">均等割付</span><span class="sxs-lookup"><span data-stu-id="7a76c-121">Force justify</span></span>  <br/> |<span data-ttu-id="7a76c-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="7a76c-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a76c-123">注釈</span><span class="sxs-lookup"><span data-stu-id="7a76c-123">Remarks</span></span>

<span data-ttu-id="7a76c-124">両端揃えの場合、段落の最終行以外の各行の単語間に空白が挿入されて、テキストの左右の両端が余白に合わせて揃えられます</span><span class="sxs-lookup"><span data-stu-id="7a76c-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="7a76c-125">均等割付の場合は、段落の最終行も含めて、すべての行の両端を揃えます。</span><span class="sxs-lookup"><span data-stu-id="7a76c-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="7a76c-126">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [HAlign] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7a76c-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7a76c-127">セル名:</span><span class="sxs-lookup"><span data-stu-id="7a76c-127">Cell name:</span></span>  <br/> | <span data-ttu-id="7a76c-128">HorzAlign [ *i* ] *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="7a76c-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7a76c-129">プログラムから、インデックスによって [HAlign] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7a76c-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7a76c-130">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7a76c-130">Section index:</span></span>  <br/> |<span data-ttu-id="7a76c-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="7a76c-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="7a76c-132">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7a76c-132">Row index:</span></span>  <br/> |<span data-ttu-id="7a76c-133">**visRowParagraph** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="7a76c-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7a76c-134">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7a76c-134">Cell index:</span></span>  <br/> |<span data-ttu-id="7a76c-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="7a76c-135">**visHorzAlign**</span></span> <br/> |
   

