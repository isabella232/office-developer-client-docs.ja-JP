---
title: '[Transparency] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: 図形のテキストの色に適用される透過性レベルを指定します。
ms.openlocfilehash: 5914a061b1bba2173b338544b05abda8780ff164
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806672"
---
# <a name="transparency-cell-character-section"></a><span data-ttu-id="b2cf0-103">[Transparency] セル ([文字] セクション)</span><span class="sxs-lookup"><span data-stu-id="b2cf0-103">Transparency Cell (Character Section)</span></span>

<span data-ttu-id="b2cf0-104">図形のテキストの色に適用される透過性レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="b2cf0-104">Determines the transparency level for a range of a shape's text color.</span></span>
  
|<span data-ttu-id="b2cf0-105">**値**</span><span class="sxs-lookup"><span data-stu-id="b2cf0-105">**Value**</span></span>|<span data-ttu-id="b2cf0-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="b2cf0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b2cf0-107">
          0 ～ 100
</span><span class="sxs-lookup"><span data-stu-id="b2cf0-107">0 - 100</span></span>  <br/> |<span data-ttu-id="b2cf0-p101">透過性をパーセントで表します。既定値は 0% (完全に不透明) です。</span><span class="sxs-lookup"><span data-stu-id="b2cf0-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2cf0-110">注釈</span><span class="sxs-lookup"><span data-stu-id="b2cf0-110">Remarks</span></span>

<span data-ttu-id="b2cf0-p102">値は、最も近い 0.5% 単位の値に丸められます。値 "100%" は完全な透明を表します。テキストが完全に透明な図形は、図面ページではテキストがない図形と同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。</span><span class="sxs-lookup"><span data-stu-id="b2cf0-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape that has completely transparent text appears the same on the drawing page as a shape that has no text, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="b2cf0-114">**テキスト**] ダイアログ ボックスで [**フォント**] タブでスライダー コントロールを使用してこの値を設定することもできます ([**ホーム**] タブで、[**フォント**の矢印] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="b2cf0-114">You can also set this value by using the slider control on the **Font** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="b2cf0-p103">[Character] セクションに複数の行が含まれる場合は、[Transparency] セルには、図形のテキストのサブ範囲に適用される書式設定情報が表示されます。複数の行が含まれない場合は、このセルには、すべての図形のテキストに対する書式設定情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2cf0-p103">If the Characters section contains multiple rows, the Transparency cell contains formatting information applied to a sub-range of a shape's text. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="b2cf0-117">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Transparency] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b2cf0-117">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2cf0-118">セル名:</span><span class="sxs-lookup"><span data-stu-id="b2cf0-118">Cell name:</span></span>  <br/> |<span data-ttu-id="b2cf0-119">Char.ColorTrans [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="b2cf0-119">Char.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b2cf0-120">プログラムから、インデックスによって [Transparency] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b2cf0-120">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2cf0-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b2cf0-121">Section index:</span></span>  <br/> |<span data-ttu-id="b2cf0-122">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="b2cf0-122">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="b2cf0-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b2cf0-123">Row index:</span></span>  <br/> |<span data-ttu-id="b2cf0-124">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="b2cf0-124">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b2cf0-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b2cf0-125">Cell index:</span></span>  <br/> |<span data-ttu-id="b2cf0-126">**visCharacterColorTrans**</span><span class="sxs-lookup"><span data-stu-id="b2cf0-126">**visCharacterColorTrans**</span></span> <br/> |
   

