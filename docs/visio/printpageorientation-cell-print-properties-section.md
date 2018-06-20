---
title: '[PrintPageOrientation] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: ページの印刷方向を、縦向きにするか横向きにするかを指定します。
ms.openlocfilehash: 2adc7dadcb3702e6c5307bb569b2ae1df7aee54e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806115"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="f0fbe-103">[PrintPageOrientation] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="f0fbe-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="f0fbe-104">ページの印刷方向を、縦向きにするか横向きにするかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f0fbe-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="f0fbe-105">**値**</span><span class="sxs-lookup"><span data-stu-id="f0fbe-105">**Value**</span></span>|<span data-ttu-id="f0fbe-106">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="f0fbe-106">**Orientation**</span></span>|<span data-ttu-id="f0fbe-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="f0fbe-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f0fbe-108">0</span><span class="sxs-lookup"><span data-stu-id="f0fbe-108">0</span></span>  <br/> | <span data-ttu-id="f0fbe-109">プリンターの用紙サイズに合わせます。</span><span class="sxs-lookup"><span data-stu-id="f0fbe-109">Same as printer</span></span>  <br/> |<span data-ttu-id="f0fbe-110">**visPPOSameAsPrinter**</span><span class="sxs-lookup"><span data-stu-id="f0fbe-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="f0fbe-111">1</span><span class="sxs-lookup"><span data-stu-id="f0fbe-111">1</span></span>  <br/> | <span data-ttu-id="f0fbe-112">縦</span><span class="sxs-lookup"><span data-stu-id="f0fbe-112">Portrait</span></span>  <br/> |<span data-ttu-id="f0fbe-113">**visPPOPortrait**</span><span class="sxs-lookup"><span data-stu-id="f0fbe-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="f0fbe-114">2</span><span class="sxs-lookup"><span data-stu-id="f0fbe-114">2</span></span>  <br/> |<span data-ttu-id="f0fbe-115">横</span><span class="sxs-lookup"><span data-stu-id="f0fbe-115">Landscape</span></span>  <br/> |<span data-ttu-id="f0fbe-116">**visPPOLandscape**</span><span class="sxs-lookup"><span data-stu-id="f0fbe-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0fbe-117">備考</span><span class="sxs-lookup"><span data-stu-id="f0fbe-117">Remarks</span></span>

<span data-ttu-id="f0fbe-118">ドキュメントに新しいページを挿入すると、この設定は既定で作業中のページで設定します。</span><span class="sxs-lookup"><span data-stu-id="f0fbe-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="f0fbe-119">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PrintPageOrientation] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="f0fbe-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0fbe-120">セル名:</span><span class="sxs-lookup"><span data-stu-id="f0fbe-120">Cell name:</span></span>  <br/> | <span data-ttu-id="f0fbe-121">PrintPageOrientation</span><span class="sxs-lookup"><span data-stu-id="f0fbe-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="f0fbe-122">プログラムから、インデックスによって [PrintPageOrientation] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="f0fbe-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0fbe-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f0fbe-123">Section index:</span></span>  <br/> |<span data-ttu-id="f0fbe-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f0fbe-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f0fbe-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f0fbe-125">Row index:</span></span>  <br/> |<span data-ttu-id="f0fbe-126">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="f0fbe-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="f0fbe-127">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f0fbe-127">Cell index:</span></span>  <br/> |<span data-ttu-id="f0fbe-128">**visPrintPropertiesPageOrientation**</span><span class="sxs-lookup"><span data-stu-id="f0fbe-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

