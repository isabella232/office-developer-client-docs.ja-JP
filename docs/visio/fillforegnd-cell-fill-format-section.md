---
title: '[FillForegnd] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: 図形の塗りつぶしのパターンで前景 (ストローク部分) に使用する色を指定します。
ms.openlocfilehash: 352fecf8d99069cfb5ebd72d295284dc03446364
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415566"
---
# <a name="fillforegnd-cell-fill-format-section"></a><span data-ttu-id="49fa3-103">[FillForegnd] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="49fa3-103">FillForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="49fa3-104">図形の塗りつぶしのパターンで前景 (ストローク部分) に使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="49fa3-104">Determines the color used for the foreground (stroke) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="49fa3-105">注釈</span><span class="sxs-lookup"><span data-stu-id="49fa3-105">Remarks</span></span>

<span data-ttu-id="49fa3-106">色を設定するには、0 ～ 23 の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="49fa3-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="49fa3-107">ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="49fa3-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="49fa3-108">ユーザー設定の色の値は rgb カラーで、数字ではなく rgb ( *r, g, b*) は [シェイプシート] ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="49fa3-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="49fa3-109">ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="49fa3-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="49fa3-110">前景の塗りつぶしの色に関する透過性を設定するには、[FillForegndTrans] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="49fa3-110">You can set the transparency of the foreground fill in the FillForegndTrans cell.</span></span>
  
<span data-ttu-id="49fa3-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FillForegnd] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="49fa3-111">To get a reference to the FillForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49fa3-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="49fa3-112">Cell name:</span></span>  <br/> |<span data-ttu-id="49fa3-113">[fillforegnd]</span><span class="sxs-lookup"><span data-stu-id="49fa3-113">FillForegnd</span></span>  <br/> |
   
<span data-ttu-id="49fa3-114">プログラムから、インデックスによって [FillForegnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="49fa3-114">To get a reference to the FillForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49fa3-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="49fa3-115">Section index:</span></span>  <br/> |<span data-ttu-id="49fa3-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="49fa3-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="49fa3-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="49fa3-117">Row index:</span></span>  <br/> |<span data-ttu-id="49fa3-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="49fa3-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="49fa3-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="49fa3-119">Cell index:</span></span>  <br/> |<span data-ttu-id="49fa3-120">**visFillForegnd**</span><span class="sxs-lookup"><span data-stu-id="49fa3-120">**visFillForegnd**</span></span> <br/> |
   

