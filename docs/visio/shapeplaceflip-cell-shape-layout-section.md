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
description: '[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、配置可能な図形をページ上で反転および回転する方法、またはそのいずれかの方法を指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: 76941b9c50e6f2c68ea9abf54e81dcd18be13a70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806402"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>[ShapePlaceFlip] セル ([図形レイアウト] セクション)

[**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときに、配置可能な図形をページ上で反転および回転する方法、またはそのいずれかの方法を指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。
  
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
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePlaceFlip] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ShapePlaceFlip  <br/> |
   
プログラムから、インデックスによって [ShapePlaceFlip] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOPlaceFlip** <br/> |
   

