---
title: '[Color] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: レイヤーの表示に使用する色を指定します。
ms.openlocfilehash: a2eef24187165cabfdfc8dee49747a2381562d3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341826"
---
# <a name="color-cell-layers-section"></a>[Color] セル ([Layers] セクション)

レイヤーの表示に使用する色を指定します。
  
## <a name="remarks"></a>解説

色を設定するには、0 ～ 23 の数値を入力します。
  
このセルの値は、[**レイヤープロパティ**] ダイアログボックス ([**ホーム**] タブの **[編集**] グループで、[**レイヤー** ] をクリックし、[**レイヤープロパティ**] をクリック) の [**レイヤーの色**] の設定に対応しています。
  
ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。 ユーザー設定の色の値は rgb カラーで、数字ではなく rgb ( *r, g, b*) は [シェイプシート] ウィンドウに表示されます。 ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。 値 255 は、そのレイヤーが無色であることを示します。 
  
レイヤーの色の透過性を設定するには、[Transparency] セルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Color] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |レイヤー. 色 [ *i* ] = ** <1>、2、3、...  <br/> |
   
プログラムから、インデックスによって [Color] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer** +  *i* = ** 0、1、2、...  <br/> |
|セル インデックス:  <br/> |**visLayerColor** <br/> |
   

