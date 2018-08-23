---
title: '[BeginArrow] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: 線の最初の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。0 ～ 45 の数値を入力するか、またはユーザーが設定した線の端点名を使用して USE 関数を入力します。[線] ダイアログ ボックスを使用することもできます。
ms.openlocfilehash: c6d5a66d76cfea61b1c9923c5b904dadec5495f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804795"
---
# <a name="beginarrow-cell-line-format-section"></a><span data-ttu-id="a28fd-104">[BeginArrow] セル ([線の書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="a28fd-104">BeginArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="a28fd-p102">線の最初の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。0 ～ 45 の数値を入力するか、またはユーザーが設定した線の端点名を使用して USE 関数を入力します。**[線]** ダイアログ ボックスを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="a28fd-p102">Indicates whether a line has an arrowhead or other line end format at its first vertex. Enter a number from 0 to 45 or the USE function with the name of a custom line end, or use the **Line** dialog box.</span></span> 
  
|<span data-ttu-id="a28fd-107">**値**</span><span class="sxs-lookup"><span data-stu-id="a28fd-107">**Value**</span></span>|<span data-ttu-id="a28fd-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="a28fd-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a28fd-109">0</span><span class="sxs-lookup"><span data-stu-id="a28fd-109">0</span></span>  <br/> | <span data-ttu-id="a28fd-110">矢印を付けません。</span><span class="sxs-lookup"><span data-stu-id="a28fd-110">No arrowhead.</span></span>  <br/> |
| <span data-ttu-id="a28fd-111">1-45</span><span class="sxs-lookup"><span data-stu-id="a28fd-111">1 - 45</span></span>  <br/> | <span data-ttu-id="a28fd-112">さまざまな矢印のスタイル。入力した値は、[**線**] ダイアログ ボックスでインデックスが付けられたエントリに対応します。</span><span class="sxs-lookup"><span data-stu-id="a28fd-112">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a28fd-113">備考</span><span class="sxs-lookup"><span data-stu-id="a28fd-113">Remarks</span></span>

<span data-ttu-id="a28fd-114">矢印のサイズは [BeginArrowSize] セルで設定します。</span><span class="sxs-lookup"><span data-stu-id="a28fd-114">The size of the arrowhead is set in the BeginArrowSize cell.</span></span>
  
<span data-ttu-id="a28fd-115">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BeginArrow] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a28fd-115">To get a reference to the BeginArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a28fd-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="a28fd-116">Cell name:</span></span>  <br/> | <span data-ttu-id="a28fd-117">BeginArrow</span><span class="sxs-lookup"><span data-stu-id="a28fd-117">BeginArrow</span></span>  <br/> |
   
<span data-ttu-id="a28fd-118">プログラムから、インデックスによって [BeginArrow] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a28fd-118">To get a reference to the BeginArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a28fd-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a28fd-119">Section index:</span></span>  <br/> |<span data-ttu-id="a28fd-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a28fd-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a28fd-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a28fd-121">Row index:</span></span>  <br/> |<span data-ttu-id="a28fd-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="a28fd-122">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="a28fd-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a28fd-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a28fd-124">**visLineBeginArrow**</span><span class="sxs-lookup"><span data-stu-id="a28fd-124">**visLineBeginArrow**</span></span> <br/> |
   

