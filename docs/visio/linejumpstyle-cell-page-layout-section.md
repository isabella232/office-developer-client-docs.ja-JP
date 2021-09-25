---
title: '[LineJumpStyle] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251646
ms.localizationpriority: medium
ms.assetid: 89f16674-ee1f-f5f9-9830-7bcc52e3a068
description: ローカルな飛び越し点のスタイルを持たない図面ページ上のすべてのコネクタに対して、飛び越し点のスタイルを指定します。
ms.openlocfilehash: 78f1003c5f1afac945edd31bf82fb64732b8da1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603670"
---
# <a name="linejumpstyle-cell-page-layout-section"></a>[LineJumpStyle] セル ([Page Layout] セクション)

ローカルな飛び越し点のスタイルを持たない図面ページ上のすべてのコネクタに対して、飛び越し点のスタイルを指定します。
  
|**値**|**飛び越し点のスタイル**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |Arc  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arc  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Gap  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |四角  <br/> |**visLOJumpStyleSquare** <br/> |
|4   <br/> |2 辺  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |台形  <br/> |**visLOJumpStyle2Point** <br/> |
|6   <br/> |4 辺  <br/> |**visLOJumpStyle3Point** <br/> |
|7   <br/> |5 辺  <br/> |**visLOJumpStyle4Point** <br/> |
|8   <br/> |6 辺  <br/> |**visLOJumpStyle5Point** <br/> |
|9   <br/> |7 辺  <br/> |**visLOJumpStyle6Point** <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[**ページ設定**] ダイアログ ボックスの [**レイアウトと経路**] タブで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックして、[**レイアウトと経路**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineJumpStyle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LineJumpStyle  <br/> |
   
プログラムから、インデックスによって [LineJumpStyle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOJumpStyle** <br/> |
   

