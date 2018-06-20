---
title: '[ShapePlaceFlip] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: 配置可能な図形を反転する方法を決定する、回転、またはその両方でページをレイアウトする図形で、[レイアウトの構成] ダイアログ ボックスを使用する場合 ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。
ms.openlocfilehash: 76941b9c50e6f2c68ea9abf54e81dcd18be13a70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806402"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>[ShapePlaceFlip] セル ([Shape Layout] セクション)

配置可能な図形を反転する方法を決定する、回転、またはその両方でページをレイアウトする図形で、[**レイアウトの構成**] ダイアログ ボックスを使用する場合 ([**デザイン**] タブの [**レイアウト**] で、**ページの再レイアウト**] をクリックし、**よりレイアウト オプション**)。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |ページの既定値を使用します。  <br/> |**visLOFlipDefault** <br/> |
|1  <br/> |水平方向に反転します。  <br/> |**visLOFlipX** <br/> |
|2  <br/> |垂直方向に反転します。  <br/> |**visLOFlipY** <br/> |
|4  <br/> |0 ～ 270°の範囲で 90°ずつ回転します。  <br/> |**visLOFlipRotate** <br/> |
|8  <br/> |反転しません。  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>注釈

[ShapePlaceFlip] セルの値を使用すると、配置可能な図形の向きを、接続先となっている別の配置可能な図形に合わせることができます。
  
図面ページでこの動作を*すべて*の図形を設定するには、[ページ レイアウト] PlaceFlip セルを使用します。 
  
取得する、[ShapePlaceFlip] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ShapePlaceFlip  <br/> |
   
プログラムから、インデックスによって [ShapePlaceFlip] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOPlaceFlip** <br/> |
   

