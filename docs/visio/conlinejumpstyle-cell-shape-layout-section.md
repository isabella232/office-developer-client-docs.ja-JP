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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415993"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>[ConLineJumpStyle] セル ([Shape Layout] セクション)

動的コネクタの飛び越し点のスタイルを指定します。
  
|**値**|**[線のジャンプ スタイル]**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |ページの既定値  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arc  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Gap  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |四角  <br/> |**visLOJumpStyleSquare** <br/> |
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

このセルの値を設定するには、動的コネクタを選択し、[開発] タブの [図形デザイン] グループ [](run-in-developer-mode-display-the-developer-tab.md)の [動作] をクリックし、[コネクタ] タブ **をクリック** します。  
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineJumpStyle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ConLineJumpStyle  <br/> |
   
プログラムから、インデックスによって [ConLineJumpStyle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  

