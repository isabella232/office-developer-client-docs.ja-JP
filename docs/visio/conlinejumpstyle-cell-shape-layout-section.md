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
ms.openlocfilehash: ae8af4e326a6c895b3617a4869f98eaf0db68db1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360061"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>[ConLineJumpStyle] セル ([Shape Layout] セクション)

動的コネクタの飛び越し点のスタイルを指定します。
  
|**値**|**飛び越し点のスタイル**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |ページの既定値  <br/> |**visLOJumpStyleDefault** <br/> |
|1-d  <br/> |円弧  <br/> |**visLOJumpStyleArc** <br/> |
|pbm-2  <br/> |Gap  <br/> |**visLOJumpStyleGap** <br/> |
|1/3  <br/> |四角  <br/> |**visLOJumpStyleSquare** <br/> |
|2/4  <br/> |三角形  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |台形  <br/> |**visLOJumpStyle2Point** <br/> |
|シックス  <br/> |4 辺  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 辺  <br/> |**visLOJumpStyle4Point** <br/> |
|~  <br/> |6 辺  <br/> |**visLOJumpStyle5Point** <br/> |
|i-9  <br/> |7 辺  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOJumpStyle** <br/> |
   
## <a name="remarks"></a>解説

このセルの値は、動的コネクタを選択し、[[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で [**基本動作**] をクリックし、[**コネクタ**] タブをクリックして設定することもできます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineJumpStyle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[conlinejumpstyle]  <br/> |
   
プログラムから、インデックスによって [ConLineJumpStyle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  

