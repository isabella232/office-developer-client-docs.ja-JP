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
ms.openlocfilehash: b6728d44c71f6403e772a6a7e730ba3c18d9eb48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805024"
---
# <a name="color-cell-layers-section"></a>[Color] セル ([Layers] セクション)

レイヤーの表示に使用する色を指定します。
  
## <a name="remarks"></a>注釈

色を設定するには、0 ～ 23 の数値を入力します。
  
このセルの値は、 **[レイヤー プロパティ**] ダイアログ ボックスで**レイヤーの色**の設定に対応する ([**ホーム**] タブの [**編集**]、[**レイヤー** ] をクリックし、[**レイヤー プロパティ**] をクリック) します。
  
独自の色を入力するには、RGB または HSL 関数を使用します。 その RGB カラーでは、ユーザー設定の色の値と、数値ではなく RGB ( *r, g, b*)、[シェイプ シート] ウィンドウが表示されます。 数値演算で使用する場合は、24 以上の値があるユーザー設定の色です。 255 の値は、レイヤーに色が含まれていないことを示します。 
  
レイヤーの色の透過性を設定するには、[Transparency] セルを使用します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Color] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Layers.Color [ *i* ]、 *i* = < 1 > では、2、3、.  <br/> |
   
プログラムから、インデックスによって [Color] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer** +  *i* 、 *i* = 0、1、2、.  <br/> |
|セル インデックス:  <br/> |**visLayerColor** <br/> |
   

