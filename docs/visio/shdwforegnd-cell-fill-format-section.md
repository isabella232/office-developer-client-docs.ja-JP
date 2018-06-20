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
ms.openlocfilehash: f39109a296949d23142017661bb55f0708402d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806462"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="51a0a-103">[ShdwForegnd] セル ([Fill Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="51a0a-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="51a0a-104">図形の影付きの塗りつぶしパターンに対して、前景 (ストローク) に使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="51a0a-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51a0a-105">注釈</span><span class="sxs-lookup"><span data-stu-id="51a0a-105">Remarks</span></span>

<span data-ttu-id="51a0a-106">色を設定するには、色のコレクションのインデックスである 0 ～ 23 の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="51a0a-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="51a0a-107">独自の色を入力するには、RGB または HSL 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="51a0a-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="51a0a-108">その RGB カラーでは、ユーザー設定の色の値と、数値ではなく RGB ( *r, g, b*)、[シェイプ シート] ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="51a0a-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="51a0a-109">数値演算で使用する場合は、24 以上の値があるユーザー設定の色です。</span><span class="sxs-lookup"><span data-stu-id="51a0a-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="51a0a-110">図形の影付きの塗りつぶしパターンに対する前景色の透明度は、[ShdwForegndTrans] セルで設定できます。</span><span class="sxs-lookup"><span data-stu-id="51a0a-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="51a0a-111">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShdwForegnd] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="51a0a-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51a0a-112">セル名 :</span><span class="sxs-lookup"><span data-stu-id="51a0a-112">Cell name:</span></span>  <br/> | <span data-ttu-id="51a0a-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="51a0a-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="51a0a-114">プログラムから、インデックスによって [ShdwForegnd] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="51a0a-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51a0a-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="51a0a-115">Section index:</span></span>  <br/> |<span data-ttu-id="51a0a-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="51a0a-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="51a0a-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="51a0a-117">Row index:</span></span>  <br/> |<span data-ttu-id="51a0a-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="51a0a-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="51a0a-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="51a0a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="51a0a-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="51a0a-120">**visFillShdwForegnd**</span></span> <br/> |
   

