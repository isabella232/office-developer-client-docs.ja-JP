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
ms.openlocfilehash: f7e73bea5120d878a1b2dbf553a66b349d247fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434866"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="c7693-103">[PrintPageOrientation] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="c7693-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="c7693-104">ページの印刷方向を、縦向きにするか横向きにするかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c7693-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="c7693-105">**値**</span><span class="sxs-lookup"><span data-stu-id="c7693-105">**Value**</span></span>|<span data-ttu-id="c7693-106">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="c7693-106">**Orientation**</span></span>|<span data-ttu-id="c7693-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="c7693-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c7693-108">.0</span><span class="sxs-lookup"><span data-stu-id="c7693-108">0</span></span>  <br/> | <span data-ttu-id="c7693-109">プリンターの用紙サイズに合わせます。</span><span class="sxs-lookup"><span data-stu-id="c7693-109">Same as printer</span></span>  <br/> |<span data-ttu-id="c7693-110">**vispposameasprinter**</span><span class="sxs-lookup"><span data-stu-id="c7693-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="c7693-111">1 </span><span class="sxs-lookup"><span data-stu-id="c7693-111">1</span></span>  <br/> | <span data-ttu-id="c7693-112">Portrait</span><span class="sxs-lookup"><span data-stu-id="c7693-112">Portrait</span></span>  <br/> |<span data-ttu-id="c7693-113">**visppoportrait**</span><span class="sxs-lookup"><span data-stu-id="c7693-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="c7693-114">2 </span><span class="sxs-lookup"><span data-stu-id="c7693-114">2</span></span>  <br/> |<span data-ttu-id="c7693-115">写真</span><span class="sxs-lookup"><span data-stu-id="c7693-115">Landscape</span></span>  <br/> |<span data-ttu-id="c7693-116">**visPPOLandscape**</span><span class="sxs-lookup"><span data-stu-id="c7693-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7693-117">注釈</span><span class="sxs-lookup"><span data-stu-id="c7693-117">Remarks</span></span>

<span data-ttu-id="c7693-118">文書に新しいページを挿入すると、この設定は作業中のページの設定に既定値として設定されます。</span><span class="sxs-lookup"><span data-stu-id="c7693-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="c7693-119">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PrintPageOrientation] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c7693-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7693-120">セル名:</span><span class="sxs-lookup"><span data-stu-id="c7693-120">Cell name:</span></span>  <br/> | <span data-ttu-id="c7693-121">[printpageorientation]</span><span class="sxs-lookup"><span data-stu-id="c7693-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="c7693-122">プログラムから、インデックスによって [PrintPageOrientation] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c7693-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7693-123">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c7693-123">Section index:</span></span>  <br/> |<span data-ttu-id="c7693-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c7693-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c7693-125">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c7693-125">Row index:</span></span>  <br/> |<span data-ttu-id="c7693-126">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="c7693-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="c7693-127">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c7693-127">Cell index:</span></span>  <br/> |<span data-ttu-id="c7693-128">**visPrintPropertiesPageOrientation**</span><span class="sxs-lookup"><span data-stu-id="c7693-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

