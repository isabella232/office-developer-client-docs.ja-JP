---
title: '[LineColor] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
ms.localizationpriority: medium
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: 図形の線の色を指定します。
ms.openlocfilehash: 8b3381ead5299420b429cc200daa0450f3f0c0a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618673"
---
# <a name="linecolor-cell-line-format-section"></a>[LineColor] セル ([Line Format] セクション)

図形の線の色を指定します。
  
## <a name="remarks"></a>注釈

線の色を設定するには、線の色のコレクション内でインデックスとなっている 0 ～ 23 の数値を入力します。線の色のコレクションは、[**線**] ダイアログ ボックスで参照できます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**太さ**] をポイントして、[**その他の線**] をクリックします)。[LineColor] の値は、[**線**] ダイアログ ボックスで設定することもできます。 
  
ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。 カスタム色の値は RGB 色で、数値ではなく RGB( *r, g, b*) が ShapeSheet ウィンドウに表示されます。 ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。 
  
線の色の透過性を設定するには、[LineColorTrans] セルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineColor] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LineColor  <br/> |
   
プログラムから、インデックスによって [LineColor] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLine** <br/> |
|セル インデックス:  <br/> |**visLineColor** <br/> |
   

