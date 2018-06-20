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
description: 最初の頂点には、矢印やその他の書式の端点に 1 行かどうかを示します。 0 から 45 に番号を入力、または使用して機能のユーザー設定の線の端点では、名前の線] ダイアログ ボックスを使用します。
ms.openlocfilehash: c6d5a66d76cfea61b1c9923c5b904dadec5495f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804795"
---
# <a name="beginarrow-cell-line-format-section"></a><span data-ttu-id="1738c-104">[BeginArrow] セル ([Line Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="1738c-104">BeginArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="1738c-105">最初の頂点には、矢印やその他の書式の端点に 1 行かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="1738c-105">Indicates whether a line has an arrowhead or other line end format at its first vertex.</span></span> <span data-ttu-id="1738c-106">0 から 45 に番号を入力、または使用して機能のユーザー設定の線の端点では、名前の**線**] ダイアログ ボックスを使用します。</span><span class="sxs-lookup"><span data-stu-id="1738c-106">Enter a number from 0 to 45 or the USE function with the name of a custom line end, or use the **Line** dialog box.</span></span> 
  
|<span data-ttu-id="1738c-107">**値**</span><span class="sxs-lookup"><span data-stu-id="1738c-107">**Value**</span></span>|<span data-ttu-id="1738c-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="1738c-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1738c-109">0</span><span class="sxs-lookup"><span data-stu-id="1738c-109">0</span></span>  <br/> | <span data-ttu-id="1738c-110">矢印を付けません。</span><span class="sxs-lookup"><span data-stu-id="1738c-110">No arrowhead.</span></span>  <br/> |
| <span data-ttu-id="1738c-111">1-45</span><span class="sxs-lookup"><span data-stu-id="1738c-111">1 - 45</span></span>  <br/> | <span data-ttu-id="1738c-112">さまざまな矢印のスタイル、[**線**] ダイアログ ボックス内のエントリのインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="1738c-112">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1738c-113">備考</span><span class="sxs-lookup"><span data-stu-id="1738c-113">Remarks</span></span>

<span data-ttu-id="1738c-114">矢印のサイズは [BeginArrowSize] セルで設定します。</span><span class="sxs-lookup"><span data-stu-id="1738c-114">The size of the arrowhead is set in the BeginArrowSize cell.</span></span>
  
<span data-ttu-id="1738c-115">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[BeginArrow] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="1738c-115">To get a reference to the BeginArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1738c-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="1738c-116">Cell name:</span></span>  <br/> | <span data-ttu-id="1738c-117">BeginArrow</span><span class="sxs-lookup"><span data-stu-id="1738c-117">BeginArrow</span></span>  <br/> |
   
<span data-ttu-id="1738c-118">プログラムから、インデックスによって [BeginArrow] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="1738c-118">To get a reference to the BeginArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1738c-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1738c-119">Section index:</span></span>  <br/> |<span data-ttu-id="1738c-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1738c-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1738c-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1738c-121">Row index:</span></span>  <br/> |<span data-ttu-id="1738c-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="1738c-122">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="1738c-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1738c-123">Cell index:</span></span>  <br/> |<span data-ttu-id="1738c-124">**visLineBeginArrow**</span><span class="sxs-lookup"><span data-stu-id="1738c-124">**visLineBeginArrow**</span></span> <br/> |
   

