---
title: '[Scale] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: フォントの幅を制御します。 このセルの既定値は 100% です。
ms.openlocfilehash: 60e896772ddd1d59e1a1da7f2c0e90893658c624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341630"
---
# <a name="scale-cell-character-section"></a><span data-ttu-id="cbab5-104">[Scale] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="cbab5-104">Scale Cell (Character Section)</span></span>

<span data-ttu-id="cbab5-105">フォントの幅を制御します。</span><span class="sxs-lookup"><span data-stu-id="cbab5-105">Controls the font width.</span></span> <span data-ttu-id="cbab5-106">このセルの既定値は 100% です。</span><span class="sxs-lookup"><span data-stu-id="cbab5-106">The default value for this cell is 100%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cbab5-107">解説</span><span class="sxs-lookup"><span data-stu-id="cbab5-107">Remarks</span></span>

<span data-ttu-id="cbab5-p103">フォントの幅を狭くするには、1 ～ 99% の間でパーセントを設定します。フォントの幅を広くするには、101 ～ 600% の間で設定します。</span><span class="sxs-lookup"><span data-stu-id="cbab5-p103">Set the percentage between 1% and 99% to decrease the font width. Set it between 101% and 600% to increase the font width.</span></span>
  
<span data-ttu-id="cbab5-110">このセルの値は、[**テキスト**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブで [**フォント**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="cbab5-110">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="cbab5-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Scale] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cbab5-111">To get a reference to the Scale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cbab5-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="cbab5-112">Cell name:</span></span>  <br/> |<span data-ttu-id="cbab5-113">文字 fontscale [ *i* ] *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="cbab5-113">Char.FontScale[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="cbab5-114">プログラムから、インデックスによって [Scale] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cbab5-114">To get a reference to the Scale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cbab5-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="cbab5-115">Section index:</span></span>  <br/> |<span data-ttu-id="cbab5-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="cbab5-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="cbab5-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="cbab5-117">Row index:</span></span>  <br/> |<span data-ttu-id="cbab5-118">**visRowCharacter** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="cbab5-118">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="cbab5-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="cbab5-119">Cell index:</span></span>  <br/> |<span data-ttu-id="cbab5-120">**visCharacterFontScale**</span><span class="sxs-lookup"><span data-stu-id="cbab5-120">**visCharacterFontScale**</span></span> <br/> |
   

