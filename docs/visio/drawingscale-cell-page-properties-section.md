---
title: '[DrawingScale] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm265
ms.localizationpriority: medium
ms.assetid: bc447f22-a188-2c61-e33c-df0d401a4725
description: 現在の図面縮尺で、図面単位の値を表します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。
ms.openlocfilehash: f1e0ff314aea587334550568ae5067e3acdceec4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586538"
---
# <a name="drawingscale-cell-page-properties-section"></a>[DrawingScale] セル ([Page Properties] セクション)

現在の図面縮尺で、図面単位の値を表します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。
  
プログラムで [DrawingScale] セルを設定して、ページのルーラーの単位を変更できます。次の例では、プログラムで測定単位をインチからセンチメートルに変更しています。この例の場合、**ConvertResult** メソッドを使用して、元の単位の値を、別の単位の同等な値に変換しています。 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

図面の測定方法は、[DrawingScale] セルの **Units** プロパティを検討することで決定できます。 上記のマクロを実行した後、エディターイミディエイト ウィンドウで実行Visual Basicステートメントは True を返 *します*。 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a>注釈

このセルは、[**ページ設定**] ダイアログ ボックスの設定に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**ページ設定**] 矢印をクリックします)。 
  
[DrawingScale] セルの数式の単位は、図面ウィンドウのルーラーが使用する測定単位を決定します。図面の縮尺が変更されないようにするには、次のいずれかの操作を行います。
  
- [DrawingScale] セルに表示されている距離を変えずに、異なる単位で表記します。
    
- [PageScale] セルに表示されている距離を、[DrawingScale] と同じ内容に変更します。
    
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DrawingScale] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |DrawingScale  <br/> |
   
プログラムから、インデックスによって [DrawingScale] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPage** <br/> |
|セル インデックス:  <br/> |**visPageDrawingScale** <br/> |
   

