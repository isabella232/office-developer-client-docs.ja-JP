---
title: '[VerticalAlign] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: テキスト ブロック内にあるテキストに対して、垂直方向の整列方法を指定します。
ms.openlocfilehash: cfd34f17eec597c306b69f76929877013b39015e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806768"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="52da6-103">[VerticalAlign] セル ([テキスト ブロックの書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="52da6-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="52da6-104">テキスト ブロック内にあるテキストに対して、垂直方向の整列方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="52da6-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="52da6-105">**値**</span><span class="sxs-lookup"><span data-stu-id="52da6-105">**Value**</span></span>|<span data-ttu-id="52da6-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="52da6-106">**Description**</span></span>|<span data-ttu-id="52da6-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="52da6-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="52da6-108">0</span><span class="sxs-lookup"><span data-stu-id="52da6-108">0</span></span>  <br/> | <span data-ttu-id="52da6-109">上揃え</span><span class="sxs-lookup"><span data-stu-id="52da6-109">Top</span></span>  <br/> |<span data-ttu-id="52da6-110">**visVertTop**</span><span class="sxs-lookup"><span data-stu-id="52da6-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="52da6-111">1</span><span class="sxs-lookup"><span data-stu-id="52da6-111">1</span></span>  <br/> | <span data-ttu-id="52da6-112">中央揃え</span><span class="sxs-lookup"><span data-stu-id="52da6-112">Middle</span></span>  <br/> |<span data-ttu-id="52da6-113">**visVertMiddle**</span><span class="sxs-lookup"><span data-stu-id="52da6-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="52da6-114">2</span><span class="sxs-lookup"><span data-stu-id="52da6-114">2</span></span>  <br/> | <span data-ttu-id="52da6-115">下揃え</span><span class="sxs-lookup"><span data-stu-id="52da6-115">Bottom</span></span>  <br/> |<span data-ttu-id="52da6-116">**visVertBottom**</span><span class="sxs-lookup"><span data-stu-id="52da6-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52da6-117">注釈</span><span class="sxs-lookup"><span data-stu-id="52da6-117">Remarks</span></span>

<span data-ttu-id="52da6-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [VerticalAlign] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="52da6-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52da6-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="52da6-119">Cell name:</span></span>  <br/> | <span data-ttu-id="52da6-120">VerticalAlign</span><span class="sxs-lookup"><span data-stu-id="52da6-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="52da6-121">プログラムから、インデックスによって [VerticalAlign] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="52da6-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52da6-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="52da6-122">Section index:</span></span>  <br/> |<span data-ttu-id="52da6-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="52da6-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="52da6-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="52da6-124">Row index:</span></span>  <br/> |<span data-ttu-id="52da6-125">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="52da6-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="52da6-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="52da6-126">Cell index:</span></span>  <br/> |<span data-ttu-id="52da6-127">**visTxtBlkVerticalAlign**</span><span class="sxs-lookup"><span data-stu-id="52da6-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

