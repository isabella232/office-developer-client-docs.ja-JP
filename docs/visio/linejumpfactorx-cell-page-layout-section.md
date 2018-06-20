---
title: '[LineJumpFactorX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
localization_priority: Normal
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: '[LineToLineX] セルの値を基準にして、ページ上にある水平方向の動的コネクタの飛び越し点のサイズを決定します。このセルの値には、0 ～ 10 の値を使用できますが、0 ～ 1 の数値の使用をお勧めします。'
ms.openlocfilehash: fb6205407070485a0e234ee594e84979bca40891
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805697"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a>[LineJumpFactorX] セル ([Page Layout] セクション)

[LineToLineX] セルの値を基準にして、ページ上にある水平方向の動的コネクタの飛び越し点のサイズを決定します。このセルの値には、0 ～ 10 の値を使用できますが、0 ～ 1 の数値の使用をお勧めします。
  
## <a name="remarks"></a>注釈

**[ページ設定**] ダイアログ ボックスで、[**レイアウトと経路**] タブで、このセルの値を設定することもできます ([**デザイン**] タブで、 **[ページ設定**の矢印をクリックし、[**レイアウトと経路**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineJumpFactorX] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LineJumpFactorX  <br/> |
   
プログラムから、インデックスによって [LineJumpFactorX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOJumpFactorX** <br/> |
   

