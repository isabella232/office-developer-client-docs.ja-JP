---
title: '[LineJumpStyle] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251646
localization_priority: Normal
ms.assetid: 89f16674-ee1f-f5f9-9830-7bcc52e3a068
description: ローカルな飛び越し点のスタイルを持たない図面ページ上のすべてのコネクタに対して、飛び越し点のスタイルを指定します。
ms.openlocfilehash: 96941f675b67b38a8575bd712db5ad0eb76cd50f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805711"
---
# <a name="linejumpstyle-cell-page-layout-section"></a>[LineJumpStyle] セル ([Page Layout] セクション)

ローカルな飛び越し点のスタイルを持たない図面ページ上のすべてのコネクタに対して、飛び越し点のスタイルを指定します。
  
|**値**|**飛び越し点のスタイル**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |円弧  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |円弧  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |破断  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |四角形  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |2 辺  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |台形  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 辺  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 辺  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 辺  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 辺  <br/> |**visLOJumpStyle6Point** <br/> |
   
## <a name="remarks"></a>備考

**[ページ設定**] ダイアログ ボックスで、[**レイアウトと経路**] タブで、このセルの値を設定することもできます ([**デザイン**] タブで、 **[ページ設定**の矢印をクリックし、[**レイアウトと経路**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineJumpStyle] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LineJumpStyle  <br/> |
   
プログラムから、インデックスによって [LineJumpStyle] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOJumpStyle** <br/> |
   

