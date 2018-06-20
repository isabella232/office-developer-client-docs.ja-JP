---
title: '[DoubleULine] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: テキストの範囲に二重下線を付けるかどうかを指定します。
ms.openlocfilehash: d0a07d8c86bd7e9ed3eb14074dda164f82c92475
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805277"
---
# <a name="doubleuline-cell-character-section"></a><span data-ttu-id="e034f-103">[DoubleULine] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="e034f-103">DoubleULine Cell (Character Section)</span></span>

<span data-ttu-id="e034f-104">テキストの範囲に二重下線を付けるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e034f-104">Determines whether the range of text has a double underline below it.</span></span>
  
|<span data-ttu-id="e034f-105">**値**</span><span class="sxs-lookup"><span data-stu-id="e034f-105">**Value**</span></span>|<span data-ttu-id="e034f-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="e034f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e034f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e034f-107">TRUE</span></span>  <br/> |<span data-ttu-id="e034f-108">テキストに二重下線を付けます。</span><span class="sxs-lookup"><span data-stu-id="e034f-108">Text has a double underline below it.</span></span>  <br/> |
|<span data-ttu-id="e034f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e034f-109">FALSE</span></span>  <br/> |<span data-ttu-id="e034f-110">テキストに二重下線を付けません。</span><span class="sxs-lookup"><span data-stu-id="e034f-110">Text does not have a double underline below it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e034f-111">注釈</span><span class="sxs-lookup"><span data-stu-id="e034f-111">Remarks</span></span>

<span data-ttu-id="e034f-p101">[Character] セクションに行が複数存在する場合、[DoubleULine] セルには図形のテキストのサブ範囲に適用される書式設定情報が表示されます。複数の行が含まれない場合は、このセルには、すべての図形のテキストに対する書式設定情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e034f-p101">The DoubleULine cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="e034f-114">**テキスト**] ダイアログ ボックスを使用してこのセルの値を設定することもできます ([**ホーム**] タブで**フォント**の矢印をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="e034f-114">You can also set the value of this cell by using the **Text** dialog box (click the **Font** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="e034f-115">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[DoubleULine] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="e034f-115">To get a reference to the DoubleULine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e034f-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="e034f-116">Cell name:</span></span>  <br/> |<span data-ttu-id="e034f-117">Char.DblUnderline [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="e034f-117">Char.DblUnderline[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e034f-118">プログラムから、インデックスによって [DoubleULine] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="e034f-118">To get a reference to the DoubleULine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e034f-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e034f-119">Section index:</span></span>  <br/> |<span data-ttu-id="e034f-120">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="e034f-120">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="e034f-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e034f-121">Row index:</span></span>  <br/> |<span data-ttu-id="e034f-122">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="e034f-122">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e034f-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e034f-123">Cell index:</span></span>  <br/> |<span data-ttu-id="e034f-124">**visCharacterDblUnderline**</span><span class="sxs-lookup"><span data-stu-id="e034f-124">**visCharacterDblUnderline**</span></span> <br/> |
   

