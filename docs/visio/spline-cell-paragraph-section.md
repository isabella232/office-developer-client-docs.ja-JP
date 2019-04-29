---
title: '[SpLine] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
localization_priority: Normal
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: テキスト内の任意の行から次の行までの距離を、テキスト行の高さを 100% としてパーセントで表します。
ms.openlocfilehash: 82b2604a62608c0cc4333892d678b1eb886a9c7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434915"
---
# <a name="spline-cell-paragraph-section"></a><span data-ttu-id="7e757-103">[SpLine] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="7e757-103">SpLine Cell (Paragraph Section)</span></span>

<span data-ttu-id="7e757-104">テキスト内の任意の行から次の行までの距離を、テキスト行の高さを 100% としてパーセントで表します。</span><span class="sxs-lookup"><span data-stu-id="7e757-104">Determines the distance between one line of text and the next, expressed as a percentage, where 100% is the height of a text line.</span></span>
  
|<span data-ttu-id="7e757-105">**値**</span><span class="sxs-lookup"><span data-stu-id="7e757-105">**Value**</span></span>|<span data-ttu-id="7e757-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="7e757-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7e757-107">\>.0</span><span class="sxs-lookup"><span data-stu-id="7e757-107">\>0</span></span>  <br/> | <span data-ttu-id="7e757-108">フォント サイズに関係なく、絶対間隔になります。</span><span class="sxs-lookup"><span data-stu-id="7e757-108">Absolute spacing, regardless of font size</span></span>  <br/> |
| <span data-ttu-id="7e757-109">i</span><span class="sxs-lookup"><span data-stu-id="7e757-109">=0</span></span>  <br/> | <span data-ttu-id="7e757-110">ベタ組みで設定されます (間隔 = フォント サイズの 100%)。</span><span class="sxs-lookup"><span data-stu-id="7e757-110">Set solid (spacing = 100% of font size)</span></span>  <br/> |
| <span data-ttu-id="7e757-111">\<.0</span><span class="sxs-lookup"><span data-stu-id="7e757-111">\<0</span></span>  <br/> | <span data-ttu-id="7e757-112">フォント サイズのパーセントです。たとえば -120% を指定すると、文字サイズの 120% で間隔が設定されます。</span><span class="sxs-lookup"><span data-stu-id="7e757-112">A percentage of font size (for example, -120% yields 120% spacing)</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e757-113">注釈</span><span class="sxs-lookup"><span data-stu-id="7e757-113">Remarks</span></span>

<span data-ttu-id="7e757-114">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SpLine] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7e757-114">To get a reference to the SpLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e757-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="7e757-115">Cell name:</span></span>  <br/> | <span data-ttu-id="7e757-116">書式.</span><span class="sxs-lookup"><span data-stu-id="7e757-116">Para.</span></span> <span data-ttu-id="7e757-117">スプライン [ *i* ] = \*\* <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="7e757-117">SpLine [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7e757-118">プログラムから、インデックスによって [SpLine] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7e757-118">To get a reference to the SpLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e757-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7e757-119">Section index:</span></span>  <br/> |<span data-ttu-id="7e757-120">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="7e757-120">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="7e757-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7e757-121">Row index:</span></span>  <br/> |<span data-ttu-id="7e757-122">**visRowParagraph** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="7e757-122">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7e757-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7e757-123">Cell index:</span></span>  <br/> |<span data-ttu-id="7e757-124">**visSpaceLine**</span><span class="sxs-lookup"><span data-stu-id="7e757-124">**visSpaceLine**</span></span> <br/> |
   

