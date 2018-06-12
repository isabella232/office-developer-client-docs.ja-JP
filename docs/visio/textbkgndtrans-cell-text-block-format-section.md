---
title: '[TextBkgndTrans] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
localization_priority: Normal
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: 図形のテキスト ブロックの背景色に適用される透過性レベルを指定します。
ms.openlocfilehash: d9fee430cb2ccd19e8d6069e7561a8fef409a62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806628"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a><span data-ttu-id="61859-103">[TextBkgndTrans] セル ([Text Block Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="61859-103">TextBkgndTrans Cell (Text Block Format Section)</span></span>

<span data-ttu-id="61859-104">図形のテキスト ブロックの背景色に適用される透過性レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="61859-104">Determines the transparency level for the background color of the shape's text block.</span></span>
  
|<span data-ttu-id="61859-105">**値**</span><span class="sxs-lookup"><span data-stu-id="61859-105">**Value**</span></span>|<span data-ttu-id="61859-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="61859-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61859-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="61859-107">0 - 100</span></span>  <br/> |<span data-ttu-id="61859-p101">透過性をパーセントで表します。既定値は 0% (完全に不透明) です。</span><span class="sxs-lookup"><span data-stu-id="61859-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61859-110">注釈</span><span class="sxs-lookup"><span data-stu-id="61859-110">Remarks</span></span>

<span data-ttu-id="61859-p102">値は、最も近い 0.5% 単位の値に丸められます。値 "100%" は完全な透明を表します。テキストの背景が完全に透明な図形は、図面ページでは背景がない図形と同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。</span><span class="sxs-lookup"><span data-stu-id="61859-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape that has a completely transparent text background appears the same on the drawing page as a shape that has no text background, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="61859-114">[**フォント**] タブ、[**テキスト**] ダイアログ ボックスのスライダー コントロールを使用してこの値を設定することもできます ([**ホーム**] タブで、[**フォント**の矢印] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="61859-114">You can also set this value using the slider control on the **Font** tab of the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="61859-115">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[TextBkgndTrans] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="61859-115">To get a reference to the TextBkgndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61859-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="61859-116">Cell name:</span></span>  <br/> |<span data-ttu-id="61859-117">TextBkgndTrans</span><span class="sxs-lookup"><span data-stu-id="61859-117">TextBkgndTrans</span></span>  <br/> |
   
<span data-ttu-id="61859-118">プログラムから、インデックスによって [TextBkgndTrans] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="61859-118">To get a reference to the TextBkgndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61859-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="61859-119">Section index:</span></span>  <br/> |<span data-ttu-id="61859-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="61859-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="61859-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="61859-121">Row index:</span></span>  <br/> |<span data-ttu-id="61859-122">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="61859-122">**visRowText**</span></span> <br/> |
|<span data-ttu-id="61859-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="61859-123">Cell index:</span></span>  <br/> |<span data-ttu-id="61859-124">**visTxtBlkBkgndTrans**</span><span class="sxs-lookup"><span data-stu-id="61859-124">**visTxtBlkBkgndTrans**</span></span> <br/> |
   

