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
ms.openlocfilehash: 8a3a5f93ff096e42ba3c13b671b46bf1cf97df82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316507"
---
# <a name="drawingscale-cell-page-properties-section"></a><span data-ttu-id="e72e8-104">[DrawingScale] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="e72e8-104">DrawingScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="e72e8-p102">現在の図面縮尺で、図面単位の値を表します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。</span><span class="sxs-lookup"><span data-stu-id="e72e8-p102">Represents the value of the drawing unit in the current drawing scale. The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
<span data-ttu-id="e72e8-107">プログラムで [DrawingScale] セルを設定して、ページのルーラーの単位を変更できます。</span><span class="sxs-lookup"><span data-stu-id="e72e8-107">You can set the DrawingScale cell to change the units of a page's rulers from a program.</span></span> <span data-ttu-id="e72e8-108">次の例では、プログラムで測定単位をインチからセンチメートルに変更しています。</span><span class="sxs-lookup"><span data-stu-id="e72e8-108">Here is an example of changing the measurement units from inches to centimeters from a program.</span></span> <span data-ttu-id="e72e8-109">この例の場合、**ConvertResult** メソッドを使用して、元の単位の値を、別の単位の同等な値に変換しています。</span><span class="sxs-lookup"><span data-stu-id="e72e8-109">In this case, we use the **ConvertResult** method to keep the distance the same but express it in different units.</span></span> 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

<span data-ttu-id="e72e8-110">図面の測定方法は、[DrawingScale] セルの **Units** プロパティを検討することで決定できます。</span><span class="sxs-lookup"><span data-stu-id="e72e8-110">You can determine the measurement system in a drawing by examining the **Units** property of the DrawingScale cell.</span></span> <span data-ttu-id="e72e8-111">上記のマクロを実行した後、Visual Basic Editor の [イミディエイト] ウィンドウで次のステートメントを実行すると、 *True*が返されます。</span><span class="sxs-lookup"><span data-stu-id="e72e8-111">After running the above macro the following statement executed in the Visual Basic Editor Immediate window will return  *True*  .</span></span> 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a><span data-ttu-id="e72e8-112">解説</span><span class="sxs-lookup"><span data-stu-id="e72e8-112">Remarks</span></span>

<span data-ttu-id="e72e8-113">このセルは、[**ページ設定**] ダイアログ ボックスの設定に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**ページ設定**] 矢印をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="e72e8-113">This cell corresponds to the settings in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="e72e8-p105">[DrawingScale] セルの数式の単位は、図面ウィンドウのルーラーが使用する測定単位を決定します。図面の縮尺が変更されないようにするには、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="e72e8-p105">The units of the formula in the DrawingScale cell determine the measurement units used by the rulers in the drawing window. If you do not want to also change the drawing's scale, you can do one of the following:</span></span>
  
- <span data-ttu-id="e72e8-116">[DrawingScale] セルに表示されている距離を変えずに、異なる単位で表記します。</span><span class="sxs-lookup"><span data-stu-id="e72e8-116">Keep the distance expressed in the DrawingScale cell the same but express it in different units.</span></span>
    
- <span data-ttu-id="e72e8-117">[PageScale] セルに表示されている距離を、[DrawingScale] と同じ内容に変更します。</span><span class="sxs-lookup"><span data-stu-id="e72e8-117">Change the distance expressed in the PageScale cell by the same factor that you change DrawingScale.</span></span>
    
<span data-ttu-id="e72e8-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DrawingScale] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e72e8-118">To get a reference to the DrawingScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e72e8-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="e72e8-119">Cell name:</span></span>  <br/> |<span data-ttu-id="e72e8-120">drawingscale]</span><span class="sxs-lookup"><span data-stu-id="e72e8-120">DrawingScale</span></span>  <br/> |
   
<span data-ttu-id="e72e8-121">プログラムから、インデックスによって [DrawingScale] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e72e8-121">To get a reference to the DrawingScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e72e8-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e72e8-122">Section index:</span></span>  <br/> |<span data-ttu-id="e72e8-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e72e8-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e72e8-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e72e8-124">Row index:</span></span>  <br/> |<span data-ttu-id="e72e8-125">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="e72e8-125">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="e72e8-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e72e8-126">Cell index:</span></span>  <br/> |<span data-ttu-id="e72e8-127">**vispageドローイング scale**</span><span class="sxs-lookup"><span data-stu-id="e72e8-127">**visPageDrawingScale**</span></span> <br/> |
   

