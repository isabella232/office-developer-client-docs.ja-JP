---
title: '[TextDirection] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: テキスト ブロック内にある文字の方向を指定します。
ms.openlocfilehash: 559a2930d9ef62612cabab79ccf55ca2c30e877b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332376"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="40aa2-103">[TextDirection] セル ([Text Block Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="40aa2-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="40aa2-104">テキスト ブロック内にある文字の方向を指定します。</span><span class="sxs-lookup"><span data-stu-id="40aa2-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="40aa2-105">**値**</span><span class="sxs-lookup"><span data-stu-id="40aa2-105">**Value**</span></span>|<span data-ttu-id="40aa2-106">**Direction**</span><span class="sxs-lookup"><span data-stu-id="40aa2-106">**Direction**</span></span>|<span data-ttu-id="40aa2-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="40aa2-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="40aa2-108">.0</span><span class="sxs-lookup"><span data-stu-id="40aa2-108">0</span></span>  <br/> | <span data-ttu-id="40aa2-109">横方向</span><span class="sxs-lookup"><span data-stu-id="40aa2-109">Horizontal</span></span>  <br/> |<span data-ttu-id="40aa2-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="40aa2-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="40aa2-111">1-d</span><span class="sxs-lookup"><span data-stu-id="40aa2-111">1</span></span>  <br/> | <span data-ttu-id="40aa2-112">縦</span><span class="sxs-lookup"><span data-stu-id="40aa2-112">Vertical</span></span>  <br/> |<span data-ttu-id="40aa2-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="40aa2-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40aa2-114">解説</span><span class="sxs-lookup"><span data-stu-id="40aa2-114">Remarks</span></span>

<span data-ttu-id="40aa2-115">Visio Version 5.0 日本語版では、このセルの値は [Miscellaneous] セクションの [VerticalText] セルに格納されていました。</span><span class="sxs-lookup"><span data-stu-id="40aa2-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="40aa2-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TextDirection] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="40aa2-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40aa2-117">セル名 :</span><span class="sxs-lookup"><span data-stu-id="40aa2-117">Cell name:</span></span>  <br/> | <span data-ttu-id="40aa2-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="40aa2-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="40aa2-119">プログラムから、インデックスによって [TextDirection] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="40aa2-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40aa2-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="40aa2-120">Section index:</span></span>  <br/> |<span data-ttu-id="40aa2-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="40aa2-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="40aa2-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="40aa2-122">Row index:</span></span>  <br/> |<span data-ttu-id="40aa2-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="40aa2-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="40aa2-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="40aa2-124">Cell index:</span></span>  <br/> |<span data-ttu-id="40aa2-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="40aa2-125">**visTxtBlkDirection**</span></span> <br/> |
   

