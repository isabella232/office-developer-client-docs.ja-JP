---
title: '[FillForegnd] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
ms.localizationpriority: medium
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: 図形の塗りつぶしのパターンで前景 (ストローク部分) に使用する色を指定します。
ms.openlocfilehash: fa561477a2357d797ecdf03a850d296c899801ca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574245"
---
# <a name="fillforegnd-cell-fill-format-section"></a>[FillForegnd] セル ([Fill Format] セクション)

図形の塗りつぶしのパターンで前景 (ストローク部分) に使用する色を指定します。
  
## <a name="remarks"></a>注釈

色を設定するには、0 ～ 23 の数値を入力します。
  
ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。 カスタム色の値は RGB 色で、数値ではなく RGB( *r, g, b*) が ShapeSheet ウィンドウに表示されます。 ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。 
  
前景の塗りつぶしの色に関する透過性を設定するには、[FillForegndTrans] セルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FillForegnd] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |FillForegnd  <br/> |
   
プログラムから、インデックスによって [FillForegnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowFill** <br/> |
|セル インデックス:  <br/> |**visFillForegnd** <br/> |
   

