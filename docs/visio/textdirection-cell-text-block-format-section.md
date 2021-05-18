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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406228"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="f7727-103">[TextDirection] セル ([Text Block Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="f7727-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="f7727-104">テキスト ブロック内にある文字の方向を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7727-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="f7727-105">**値**</span><span class="sxs-lookup"><span data-stu-id="f7727-105">**Value**</span></span>|<span data-ttu-id="f7727-106">**[方向]**</span><span class="sxs-lookup"><span data-stu-id="f7727-106">**Direction**</span></span>|<span data-ttu-id="f7727-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="f7727-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f7727-108">0</span><span class="sxs-lookup"><span data-stu-id="f7727-108">0</span></span>  <br/> | <span data-ttu-id="f7727-109">横方向</span><span class="sxs-lookup"><span data-stu-id="f7727-109">Horizontal</span></span>  <br/> |<span data-ttu-id="f7727-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="f7727-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="f7727-111">1</span><span class="sxs-lookup"><span data-stu-id="f7727-111">1</span></span>  <br/> | <span data-ttu-id="f7727-112">縦</span><span class="sxs-lookup"><span data-stu-id="f7727-112">Vertical</span></span>  <br/> |<span data-ttu-id="f7727-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="f7727-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7727-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f7727-114">Remarks</span></span>

<span data-ttu-id="f7727-115">Visio Version 5.0 日本語版では、このセルの値は [Miscellaneous] セクションの [VerticalText] セルに格納されていました。</span><span class="sxs-lookup"><span data-stu-id="f7727-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="f7727-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TextDirection] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f7727-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f7727-117">セル名 :</span><span class="sxs-lookup"><span data-stu-id="f7727-117">Cell name:</span></span>  <br/> | <span data-ttu-id="f7727-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="f7727-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="f7727-119">プログラムから、インデックスによって [TextDirection] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7727-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f7727-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f7727-120">Section index:</span></span>  <br/> |<span data-ttu-id="f7727-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f7727-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f7727-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f7727-122">Row index:</span></span>  <br/> |<span data-ttu-id="f7727-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="f7727-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="f7727-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f7727-124">Cell index:</span></span>  <br/> |<span data-ttu-id="f7727-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="f7727-125">**visTxtBlkDirection**</span></span> <br/> |
   

