---
title: '[ShdwForegnd] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: 図形の影付きの塗りつぶしパターンに対して、前景 (ストローク) に使用する色を指定します。
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349106"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="e9aa8-103">[ShdwForegnd] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="e9aa8-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="e9aa8-104">図形の影付きの塗りつぶしパターンに対して、前景 (ストローク) に使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9aa8-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9aa8-105">解説</span><span class="sxs-lookup"><span data-stu-id="e9aa8-105">Remarks</span></span>

<span data-ttu-id="e9aa8-106">色を設定するには、色のコレクションのインデックスである 0 ～ 23 の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9aa8-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="e9aa8-107">ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="e9aa8-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="e9aa8-108">ユーザー設定の色の値は rgb カラーで、数字ではなく rgb ( *r, g, b*) は [シェイプシート] ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e9aa8-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="e9aa8-109">ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9aa8-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="e9aa8-110">図形の影付きの塗りつぶしパターンに対する前景色の透明度は、[ShdwForegndTrans] セルで設定できます。</span><span class="sxs-lookup"><span data-stu-id="e9aa8-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="e9aa8-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwForegnd] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e9aa8-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9aa8-112">セル名 :</span><span class="sxs-lookup"><span data-stu-id="e9aa8-112">Cell name:</span></span>  <br/> | <span data-ttu-id="e9aa8-113">[shdwforegnd]</span><span class="sxs-lookup"><span data-stu-id="e9aa8-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="e9aa8-114">プログラムから、インデックスによって [ShdwForegnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9aa8-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9aa8-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e9aa8-115">Section index:</span></span>  <br/> |<span data-ttu-id="e9aa8-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e9aa8-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e9aa8-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e9aa8-117">Row index:</span></span>  <br/> |<span data-ttu-id="e9aa8-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="e9aa8-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="e9aa8-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e9aa8-119">Cell index:</span></span>  <br/> |<span data-ttu-id="e9aa8-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="e9aa8-120">**visFillShdwForegnd**</span></span> <br/> |
   

