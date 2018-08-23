---
title: '[ConLineJumpStyle] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251655
localization_priority: Normal
ms.assetid: baa05a50-97d0-3769-635e-0ea20317d59a
description: 動的コネクタの飛び越し点のスタイルを指定します。
ms.openlocfilehash: d3e27ddb6689fb5635674b3c4a8462fe587bce7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805094"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>[ConLineJumpStyle] セル ([図形レイアウト] セクション)

動的コネクタの飛び越し点のスタイルを指定します。
  
|**値**|**飛び越し点のスタイル**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |ページの既定値  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |円弧  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |破断  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |四角形  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |三角形  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |台形  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 辺  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 辺  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 辺  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 辺  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOJumpStyle** <br/> |
   
## <a name="remarks"></a>注釈

設定できますでは、このセルの値、動的コネクタを**図形のデザイン**] で [[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、**動作**をクリックして、[**コネクタ**] タブをクリックします。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineJumpStyle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ConLineJumpStyle  <br/> |
   
プログラムから、インデックスによって [ConLineJumpStyle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  

