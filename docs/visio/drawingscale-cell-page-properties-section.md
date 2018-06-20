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
# <a name="drawingscale-cell-page-properties-section"></a>[DrawingScale] セル ([Page Properties] セクション)

現在の図面縮尺で、図面単位の値を表します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。
  
DrawingScale セルをプログラムから、ページのルーラーの単位を変更するを設定することができます。 ここでは、寸法の単位をインチからプログラムからセンチメートルに変更する例です。 この例では、メソッドを使用して、 **ConvertResult**同じ距離を維持しますが、それを別の単位で表現します。 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

DrawingScale セルの**Units**プロパティを調べることによって、図面の計測システムを指定できます。 エディターの Visual Basic のイミディ エイトを実行する次のステートメント、上記のマクロを実行した後ウィンドウは*True*を返します。 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a>備考

このセルは、[**ページ設定**] ダイアログ ボックスの設定に対応して ([**ホーム**] タブの **[ページ設定**の矢印をクリック) します。 
  
[DrawingScale] セルの数式の単位は、図面ウィンドウのルーラーが使用する測定単位を決定します。図面の縮尺が変更されないようにするには、次のいずれかの操作を行います。
  
- [DrawingScale] セルに表示されている距離を変えずに、異なる単位で表記します。
    
- [PageScale] セルに表示されている距離を、[DrawingScale] と同じ内容に変更します。
    
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[DrawingScale] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |DrawingScale  <br/> |
   
プログラムから、インデックスによって [DrawingScale] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPage** <br/> |
|セル インデックス:  <br/> |**visPageDrawingScale** <br/> |
   

