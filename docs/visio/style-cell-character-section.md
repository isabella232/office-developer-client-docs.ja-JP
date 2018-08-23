---
title: '[Style] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
localization_priority: Normal
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: 図形のテキスト ブロック内にあるテキストの範囲に適用される文字の書式を表示します。
ms.openlocfilehash: 48bda5eb798f439e2616b2b910d7ec5ac719d060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806569"
---
# <a name="style-cell-character-section"></a><span data-ttu-id="f9643-103">[Style] セル ([文字] セクション)</span><span class="sxs-lookup"><span data-stu-id="f9643-103">Style Cell (Character Section)</span></span>

<span data-ttu-id="f9643-104">図形のテキスト ブロック内にあるテキストの範囲に適用される文字の書式を表示します。</span><span class="sxs-lookup"><span data-stu-id="f9643-104">Shows the character formatting applied to a range of text in the shape's text block.</span></span>
  
|<span data-ttu-id="f9643-105">**Style**</span><span class="sxs-lookup"><span data-stu-id="f9643-105">**Style**</span></span>|<span data-ttu-id="f9643-106">**値**</span><span class="sxs-lookup"><span data-stu-id="f9643-106">**Value**</span></span>|<span data-ttu-id="f9643-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="f9643-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f9643-108">太字</span><span class="sxs-lookup"><span data-stu-id="f9643-108">Bold</span></span>  <br/> | <span data-ttu-id="f9643-109">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="f9643-109">&amp;H1</span></span>  <br/> |<span data-ttu-id="f9643-110">**visBold**</span><span class="sxs-lookup"><span data-stu-id="f9643-110">**visBold**</span></span> <br/> |
| <span data-ttu-id="f9643-111">イタリック</span><span class="sxs-lookup"><span data-stu-id="f9643-111">Italic</span></span>  <br/> | <span data-ttu-id="f9643-112">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="f9643-112">&amp;H2</span></span>  <br/> |<span data-ttu-id="f9643-113">**visItalic**</span><span class="sxs-lookup"><span data-stu-id="f9643-113">**visItalic**</span></span> <br/> |
| <span data-ttu-id="f9643-114">下線</span><span class="sxs-lookup"><span data-stu-id="f9643-114">Underline</span></span>  <br/> | <span data-ttu-id="f9643-115">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="f9643-115">&amp;H4</span></span>  <br/> |<span data-ttu-id="f9643-116">**visUnderLine**</span><span class="sxs-lookup"><span data-stu-id="f9643-116">**visUnderLine**</span></span> <br/> |
| <span data-ttu-id="f9643-117">小型英文字</span><span class="sxs-lookup"><span data-stu-id="f9643-117">Small caps</span></span>  <br/> | <span data-ttu-id="f9643-118">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="f9643-118">&amp;H8</span></span>  <br/> |<span data-ttu-id="f9643-119">**visSmallCaps**</span><span class="sxs-lookup"><span data-stu-id="f9643-119">**visSmallCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9643-120">備考</span><span class="sxs-lookup"><span data-stu-id="f9643-120">Remarks</span></span>

<span data-ttu-id="f9643-p101">[Character] セクションに複数の行が含まれる場合は、[Style] セルには、図形のテキストのサブ範囲に適用される書式設定情報が表示されます。複数の行が含まれない場合は、このセルには、すべての図形のテキストに対する書式設定情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9643-p101">The Style cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="f9643-123">値は、各ビットが文字スタイルを示す 2 進数を表します。</span><span class="sxs-lookup"><span data-stu-id="f9643-123">The value represents a binary number in which each bit indicates a character style.</span></span> <span data-ttu-id="f9643-124">たとえば、3 の値は、斜体と太字の両方で書式設定された文字列を表します。</span><span class="sxs-lookup"><span data-stu-id="f9643-124">For example, a value of 3 represents text formatted in both italic and bold.</span></span> <span data-ttu-id="f9643-125">スタイルの値が 0 の場合は、テキストはプレーン テキストつまり書式設定されていない、します。</span><span class="sxs-lookup"><span data-stu-id="f9643-125">If the value of Style is 0, the text is plain, or unformatted.</span></span> <span data-ttu-id="f9643-126">ブール値のビットを使用して特定の書式をテストすることができます\*関数です。</span><span class="sxs-lookup"><span data-stu-id="f9643-126">You can test for a particular format using Boolean BIT\* functions.</span></span> <span data-ttu-id="f9643-127">これらの関数の詳細について、プログラミングに関するマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9643-127">See your programming documentation for details about these functions.</span></span>
  
<span data-ttu-id="f9643-128">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Style] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f9643-128">To get a reference to the Style cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f9643-129">セル名:</span><span class="sxs-lookup"><span data-stu-id="f9643-129">Cell name:</span></span>  <br/> | <span data-ttu-id="f9643-130">Char.Style [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="f9643-130">Char.Style[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f9643-131">プログラムから、インデックスによって [Style] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f9643-131">To get a reference to the Style cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f9643-132">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f9643-132">Section index:</span></span>  <br/> |<span data-ttu-id="f9643-133">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="f9643-133">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="f9643-134">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f9643-134">Row index:</span></span>  <br/> |<span data-ttu-id="f9643-135">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="f9643-135">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f9643-136">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f9643-136">Cell index:</span></span>  <br/> |<span data-ttu-id="f9643-137">**visCharacterStyle**</span><span class="sxs-lookup"><span data-stu-id="f9643-137">**visCharacterStyle**</span></span> <br/> |
   
 <span data-ttu-id="f9643-138">*例*</span><span class="sxs-lookup"><span data-stu-id="f9643-138">*Example*</span></span> 
  
<span data-ttu-id="f9643-139">ある図形の [Character] セクションの先頭行にある [Color] セルが、次の数式に設定されているとします。</span><span class="sxs-lookup"><span data-stu-id="f9643-139">Suppose the Color cell in the first row of a shape's Character section is set to this formula:</span></span>
  
<span data-ttu-id="f9643-140">= IF(BITAND(Char.Style,1)=1,4,3)</span><span class="sxs-lookup"><span data-stu-id="f9643-140">= IF(BITAND(Char.Style,1)=1,4,3)</span></span>
  
<span data-ttu-id="f9643-p103">図形のテキスト上にある最初の文字が太字の場合は、最初の Character プロパティ行の対象となるテキストは青 (4) になります。太字以外の場合は、テキストは緑 (3) になります。この例では、既定の色が有効であるものと仮定します。</span><span class="sxs-lookup"><span data-stu-id="f9643-p103">Then if the first character of the shape's text is bold, the text covered by the first Character properties row will be blue (4); otherwise it will be green (3). This example assumes default colors are in effect.</span></span>
  
<span data-ttu-id="f9643-p104">次の例は、プログラムの中で [Style] セルを設定するものです。先頭のステートメントは、名前によって [Style] セルを参照します。2 番目のステートメントは、インデックスによって [Style] セルを参照します。どちらのステートメントも、図形の [Character] セクションの第 2 行の対象となるテキストに対して斜体を適用します。</span><span class="sxs-lookup"><span data-stu-id="f9643-p104">The following is an example of setting the Style cell in a program. The first statement references the Style cell by name, and the second statement references the Style cell by index. Both statements apply italic to the text covered by the second row of a shape's Character section.</span></span>
  

