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
ms.openlocfilehash: 954a0cf0b80d6b675dcc016997f1923041069eac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425793"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="8c465-103">[VerticalAlign] セル ([Text Block Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="8c465-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="8c465-104">テキスト ブロック内にあるテキストに対して、垂直方向の整列方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="8c465-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="8c465-105">**値**</span><span class="sxs-lookup"><span data-stu-id="8c465-105">**Value**</span></span>|<span data-ttu-id="8c465-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="8c465-106">**Description**</span></span>|<span data-ttu-id="8c465-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="8c465-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8c465-108">.0</span><span class="sxs-lookup"><span data-stu-id="8c465-108">0</span></span>  <br/> | <span data-ttu-id="8c465-109">Top</span><span class="sxs-lookup"><span data-stu-id="8c465-109">Top</span></span>  <br/> |<span data-ttu-id="8c465-110">**visVertTop**</span><span class="sxs-lookup"><span data-stu-id="8c465-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="8c465-111">1 </span><span class="sxs-lookup"><span data-stu-id="8c465-111">1</span></span>  <br/> | <span data-ttu-id="8c465-112">区分</span><span class="sxs-lookup"><span data-stu-id="8c465-112">Middle</span></span>  <br/> |<span data-ttu-id="8c465-113">**visVertMiddle**</span><span class="sxs-lookup"><span data-stu-id="8c465-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="8c465-114">2 </span><span class="sxs-lookup"><span data-stu-id="8c465-114">2</span></span>  <br/> | <span data-ttu-id="8c465-115">下</span><span class="sxs-lookup"><span data-stu-id="8c465-115">Bottom</span></span>  <br/> |<span data-ttu-id="8c465-116">**visVertBottom**</span><span class="sxs-lookup"><span data-stu-id="8c465-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c465-117">注釈</span><span class="sxs-lookup"><span data-stu-id="8c465-117">Remarks</span></span>

<span data-ttu-id="8c465-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [VerticalAlign] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8c465-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8c465-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="8c465-119">Cell name:</span></span>  <br/> | <span data-ttu-id="8c465-120">[verticalalign]</span><span class="sxs-lookup"><span data-stu-id="8c465-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="8c465-121">プログラムから、インデックスによって [VerticalAlign] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8c465-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8c465-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8c465-122">Section index:</span></span>  <br/> |<span data-ttu-id="8c465-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8c465-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8c465-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8c465-124">Row index:</span></span>  <br/> |<span data-ttu-id="8c465-125">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="8c465-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="8c465-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8c465-126">Cell index:</span></span>  <br/> |<span data-ttu-id="8c465-127">**visTxtBlkVerticalAlign**</span><span class="sxs-lookup"><span data-stu-id="8c465-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

