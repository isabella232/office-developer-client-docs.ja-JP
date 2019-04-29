---
title: '[LineAdjustTo] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: 線を束ねるときに対象とする動的コネクタを指定します。
ms.openlocfilehash: e4fb32c0fcb488173324ea597edc2c9d13f6bfca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414026"
---
# <a name="lineadjustto-cell-page-layout-section"></a>[LineAdjustTo] セル ([Page Layout] セクション)

線を束ねるときに対象とする動的コネクタを指定します。
  
|**値**|**セレクター**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |迂回方法の既定値に合わせる  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1   <br/> |近接しているすべての線  <br/> |**visPLOLineAdjustToAll** <br/> |
|2   <br/> |なし  <br/> |**visPLOLineAdjustToNone** <br/> |
|3   <br/> |関連付けられている線  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[**ページ設定**] ダイアログ ボックスの [**レイアウトと経路**] タブで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックして、[**レイアウトと経路**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineAdjustTo] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[lineadjustto]  <br/> |
   
プログラムから、インデックスによって [LineAdjustTo] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOLineAdjustTo** <br/> |
   

