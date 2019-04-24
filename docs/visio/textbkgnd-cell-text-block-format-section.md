---
title: '[TextBkgnd] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: 図形のテキストの背景色を指定します。
ms.openlocfilehash: 2450bf0cb0e013c0f9310eacfca0f5a20e7e6063
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332340"
---
# <a name="textbkgnd-cell-text-block-format-section"></a><span data-ttu-id="c89d1-103">[TextBkgnd] セル ([Text Block Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="c89d1-103">TextBkgnd Cell (Text Block Format Section)</span></span>

<span data-ttu-id="c89d1-104">図形のテキストの背景色を指定します。</span><span class="sxs-lookup"><span data-stu-id="c89d1-104">Determines the text background color for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c89d1-105">解説</span><span class="sxs-lookup"><span data-stu-id="c89d1-105">Remarks</span></span>

<span data-ttu-id="c89d1-106">[TextBkgnd] セルには、0 ～ 24、または 255 のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c89d1-106">The TextBkgnd cell can have any value from 0 through 24, or 255.</span></span> <span data-ttu-id="c89d1-107">値0と 255 ( *visTxtBlklOpaque*) は、両方とも透明なテキストの背景を示します。</span><span class="sxs-lookup"><span data-stu-id="c89d1-107">The values 0 and 255 ( *visTxtBlklOpaque*) both indicate a transparent text background.</span></span> 
  
<span data-ttu-id="c89d1-108">ユーザー設定の色を入力するには、RGB または HSL 関数に 1 を加算したもの、たとえば RGB(255,127,255)+1 を使用します。</span><span class="sxs-lookup"><span data-stu-id="c89d1-108">To enter a custom color, use the RGB or HSL function plus one—for example, RGB(255,127,255)+1.</span></span> <span data-ttu-id="c89d1-109">ユーザー設定の色の値は rgb カラーで、数字ではなく rgb ( *r, g, b*) + 1 が [シェイプシート] ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c89d1-109">The value of a custom color is its RGB color, and RGB( *r, g, b*)+1, rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="c89d1-110">ユーザー設定の色を数値演算で使用する場合は、25 以上の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c89d1-110">When used in numeric operations, custom colors have values of 25 and above.</span></span> 
  
<span data-ttu-id="c89d1-111">テキストの背景色の透過性は [TextBkgndTrans] セルで設定できます。</span><span class="sxs-lookup"><span data-stu-id="c89d1-111">You can set the transparency of the text background color in the TextBkgndTrans cell.</span></span>
  
<span data-ttu-id="c89d1-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TextBkgnd] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c89d1-112">To get a reference to the TextBkgnd cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c89d1-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="c89d1-113">Cell name:</span></span>  <br/> |<span data-ttu-id="c89d1-114">[textbkgnd]</span><span class="sxs-lookup"><span data-stu-id="c89d1-114">TextBkgnd</span></span>  <br/> |
   
<span data-ttu-id="c89d1-115">プログラムから、インデックスによって [TextBkgnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c89d1-115">To get a reference to the TextBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c89d1-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c89d1-116">Section index:</span></span>  <br/> |<span data-ttu-id="c89d1-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c89d1-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c89d1-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c89d1-118">Row index:</span></span>  <br/> |<span data-ttu-id="c89d1-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="c89d1-119">**visRowText**</span></span> <br/> |
|<span data-ttu-id="c89d1-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c89d1-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c89d1-121">**visTxtBlkBkgnd**</span><span class="sxs-lookup"><span data-stu-id="c89d1-121">**visTxtBlkBkgnd**</span></span> <br/> |
   

