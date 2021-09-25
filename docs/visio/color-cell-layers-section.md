---
title: '[Color] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
ms.localizationpriority: medium
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: レイヤーの表示に使用する色を指定します。
ms.openlocfilehash: bc0f08fbac4a542221e47f0f85b36ba15d2c1159
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577977"
---
# <a name="color-cell-layers-section"></a>[Color] セル ([Layers] セクション)

レイヤーの表示に使用する色を指定します。
  
## <a name="remarks"></a>注釈

色を設定するには、0 ～ 23 の数値を入力します。
  
このセル値は、[レイヤープロパティ] ダイアログボックスの [レイヤーの色] 設定に対応します ([ホーム] タブの [編集] グループで、[レイヤー] をクリックし、[レイヤー プロパティ] を **クリックします**)。 
  
ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。 カスタム色の値は RGB 色で、数値ではなく RGB( *r, g, b*) が ShapeSheet ウィンドウに表示されます。 ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。 値 255 は、そのレイヤーが無色であることを示します。 
  
レイヤーの色の透過性を設定するには、[Transparency] セルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Color] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Layers.Color[ *i*  ] ここで  *、i*  = <1>、2、3、..  <br/> |
   
プログラムから、インデックスによって [Color] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer**  +  *i* *=* 0, 1, 2, ...  <br/> |
|セル インデックス:  <br/> |**visLayerColor** <br/> |
   

