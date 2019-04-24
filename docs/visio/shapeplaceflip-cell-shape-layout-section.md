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
ms.openlocfilehash: 72ef1b67dd87d842e6a4372d1eb08d614f0eb2d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332670"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>[ShapePlaceFlip] セル ([Shape Layout] セクション)

[**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときに、配置可能な図形をページ上で反転および回転する方法、またはそのいずれかの方法を指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |ページの既定値を使用します。  <br/> |**visLOFlipDefault** <br/> |
|1-d  <br/> |水平方向に反転します。  <br/> |**visLOFlipX** <br/> |
|pbm-2  <br/> |垂直方向に反転します。  <br/> |**visLOFlipY** <br/> |
|2/4  <br/> |0 ～ 270°の範囲で 90°ずつ回転します。  <br/> |**visLOFlipRotate** <br/> |
|~  <br/> |反転しません。  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>解説

[ShapePlaceFlip] セルの値を使用すると、配置可能な図形の向きを、接続先となっている別の配置可能な図形に合わせることができます。
  
図面ページ上の*すべて*の図形に対してこの動作を設定するには、[ページレイアウト] セクションの [配置] セルを使用します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePlaceFlip] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[shapeplaceflip]  <br/> |
   
プログラムから、インデックスによって [ShapePlaceFlip] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**vissloフェース eflip** <br/> |
   

