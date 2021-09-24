---
title: '[Transparency] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
ms.localizationpriority: medium
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: レイヤーの色の透過性レベルを指定します。
ms.openlocfilehash: cc82d043e6a589a729a8f58c6542853e5808dd70
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549463"
---
# <a name="transparency-cell-layers-section"></a>[Transparency] セル ([Layers] セクション)

レイヤーの色の透過性レベルを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|0 ～ 100  <br/> |透過性をパーセントで表します。既定値は 0% (完全に不透明) です。  <br/> |
   
## <a name="remarks"></a>注釈

値は、最も近い 0.5% 単位の値に丸められます。値 "100%" は完全な透明を表します。完全に透明な色のレイヤーは図面ページでは無色のレイヤーと同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。この値は、[**レイヤー プロパティ**] ダイアログ ボックスのスライダー コントロールを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックして、[**レイヤー プロパティ**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Transparency] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Layers.ColorTrans[ *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Transparency] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visLayerColorTrans** <br/> |
   

