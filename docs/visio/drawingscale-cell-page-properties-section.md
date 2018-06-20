---
title: '[DrawingScale] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm265
localization_priority: Normal
ms.assetid: bc447f22-a188-2c61-e33c-df0d401a4725
description: 現在の図面縮尺で、図面単位の値を表します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。
ms.openlocfilehash: cdd3222f5e56c34ac8947c9ef5a653cfe19fbd0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805264"
---
# <a name="drawingscale-cell-page-properties-section"></a><span data-ttu-id="3c3a4-104">[DrawingScale] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="3c3a4-104">DrawingScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="3c3a4-p102">現在の図面縮尺で、図面単位の値を表します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。</span><span class="sxs-lookup"><span data-stu-id="3c3a4-p102">Represents the value of the drawing unit in the current drawing scale. The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
<span data-ttu-id="3c3a4-107">DrawingScale セルをプログラムから、ページのルーラーの単位を変更するを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="3c3a4-107">You can set the DrawingScale cell to change the units of a page's rulers from a program.</span></span> <span data-ttu-id="3c3a4-108">ここでは、寸法の単位をインチからプログラムからセンチメートルに変更する例です。</span><span class="sxs-lookup"><span data-stu-id="3c3a4-108">Here is an example of changing the measurement units from inches to centimeters from a program.</span></span> <span data-ttu-id="3c3a4-109">この例では、メソッドを使用して、 **ConvertResult**同じ距離を維持しますが、それを別の単位で表現します。</span><span class="sxs-lookup"><span data-stu-id="3c3a4-109">In this case, we use the **ConvertResult** method to keep the distance the same but express it in different units.</span></span> 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

<span data-ttu-id="3c3a4-110">DrawingScale セルの**Units**プロパティを調べることによって、図面の計測システムを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3c3a4-110">You can determine the measurement system in a drawing by examining the **Units** property of the DrawingScale cell.</span></span> <span data-ttu-id="3c3a4-111">エディターの Visual Basic のイミディ エイトを実行する次のステートメント、上記のマクロを実行した後ウィンドウは*True*を返します。</span><span class="sxs-lookup"><span data-stu-id="3c3a4-111">After running the above macro the following statement executed in the Visual Basic Editor Immediate window will return  *True*  .</span></span> 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a><span data-ttu-id="3c3a4-112">備考</span><span class="sxs-lookup"><span data-stu-id="3c3a4-112">Remarks</span></span>

<span data-ttu-id="3c3a4-113">このセルは、[**ページ設定**] ダイアログ ボックスの設定に対応して ([**ホーム**] タブの **[ページ設定**の矢印をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="3c3a4-113">This cell corresponds to the settings in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="3c3a4-p105">[DrawingScale] セルの数式の単位は、図面ウィンドウのルーラーが使用する測定単位を決定します。図面の縮尺が変更されないようにするには、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="3c3a4-p105">The units of the formula in the DrawingScale cell determine the measurement units used by the rulers in the drawing window. If you do not want to also change the drawing's scale, you can do one of the following:</span></span>
  
- <span data-ttu-id="3c3a4-116">[DrawingScale] セルに表示されている距離を変えずに、異なる単位で表記します。</span><span class="sxs-lookup"><span data-stu-id="3c3a4-116">Keep the distance expressed in the DrawingScale cell the same but express it in different units.</span></span>
    
- <span data-ttu-id="3c3a4-117">[PageScale] セルに表示されている距離を、[DrawingScale] と同じ内容に変更します。</span><span class="sxs-lookup"><span data-stu-id="3c3a4-117">Change the distance expressed in the PageScale cell by the same factor that you change DrawingScale.</span></span>
    
<span data-ttu-id="3c3a4-118">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[DrawingScale] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="3c3a4-118">To get a reference to the DrawingScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c3a4-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="3c3a4-119">Cell name:</span></span>  <br/> |<span data-ttu-id="3c3a4-120">DrawingScale</span><span class="sxs-lookup"><span data-stu-id="3c3a4-120">DrawingScale</span></span>  <br/> |
   
<span data-ttu-id="3c3a4-121">プログラムから、インデックスによって [DrawingScale] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3c3a4-121">To get a reference to the DrawingScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c3a4-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3c3a4-122">Section index:</span></span>  <br/> |<span data-ttu-id="3c3a4-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3c3a4-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3c3a4-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3c3a4-124">Row index:</span></span>  <br/> |<span data-ttu-id="3c3a4-125">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="3c3a4-125">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="3c3a4-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3c3a4-126">Cell index:</span></span>  <br/> |<span data-ttu-id="3c3a4-127">**visPageDrawingScale**</span><span class="sxs-lookup"><span data-stu-id="3c3a4-127">**visPageDrawingScale**</span></span> <br/> |
   

