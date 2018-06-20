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
ms.openlocfilehash: c238b6b2a47c968809869f8eb3e38b6f0db1dcad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806644"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="3c4d8-103">[TextDirection] セル ([Text Block Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="3c4d8-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="3c4d8-104">テキスト ブロック内にある文字の方向を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c4d8-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="3c4d8-105">**値**</span><span class="sxs-lookup"><span data-stu-id="3c4d8-105">**Value**</span></span>|<span data-ttu-id="3c4d8-106">**Direction**</span><span class="sxs-lookup"><span data-stu-id="3c4d8-106">**Direction**</span></span>|<span data-ttu-id="3c4d8-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="3c4d8-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3c4d8-108">0</span><span class="sxs-lookup"><span data-stu-id="3c4d8-108">0</span></span>  <br/> | <span data-ttu-id="3c4d8-109">横書き</span><span class="sxs-lookup"><span data-stu-id="3c4d8-109">Horizontal</span></span>  <br/> |<span data-ttu-id="3c4d8-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="3c4d8-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="3c4d8-111">1</span><span class="sxs-lookup"><span data-stu-id="3c4d8-111">1</span></span>  <br/> | <span data-ttu-id="3c4d8-112">縦書き</span><span class="sxs-lookup"><span data-stu-id="3c4d8-112">Vertical</span></span>  <br/> |<span data-ttu-id="3c4d8-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="3c4d8-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c4d8-114">備考</span><span class="sxs-lookup"><span data-stu-id="3c4d8-114">Remarks</span></span>

<span data-ttu-id="3c4d8-115">Visio Version 5.0 日本語版では、このセルの値は [Miscellaneous] セクションの [VerticalText] セルに格納されていました。</span><span class="sxs-lookup"><span data-stu-id="3c4d8-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="3c4d8-116">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[TextDirection] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="3c4d8-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3c4d8-117">セル名 :</span><span class="sxs-lookup"><span data-stu-id="3c4d8-117">Cell name:</span></span>  <br/> | <span data-ttu-id="3c4d8-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="3c4d8-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="3c4d8-119">プログラムから、インデックスによって [TextDirection] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3c4d8-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3c4d8-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3c4d8-120">Section index:</span></span>  <br/> |<span data-ttu-id="3c4d8-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3c4d8-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3c4d8-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3c4d8-122">Row index:</span></span>  <br/> |<span data-ttu-id="3c4d8-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="3c4d8-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="3c4d8-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3c4d8-124">Cell index:</span></span>  <br/> |<span data-ttu-id="3c4d8-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="3c4d8-125">**visTxtBlkDirection**</span></span> <br/> |
   

