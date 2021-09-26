---
title: '[LineAdjustTo] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
ms.localizationpriority: medium
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: 線を束ねるときに対象とする動的コネクタを指定します。
ms.openlocfilehash: 5f0d12107f760d9e442ab733fa8a03bb4bda6f55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618659"
---
# <a name="lineadjustto-cell-page-layout-section"></a>[LineAdjustTo] セル ([Page Layout] セクション)

線を束ねるときに対象とする動的コネクタを指定します。
  
|**値**|**調整**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |迂回方法の既定値に合わせる  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1  <br/> |近接しているすべての線  <br/> |**visPLOLineAdjustToAll** <br/> |
|2  <br/> |なし  <br/> |**visPLOLineAdjustToNone** <br/> |
|3  <br/> |関連付けられている線  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[**ページ設定**] ダイアログ ボックスの [**レイアウトと経路**] タブで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックして、[**レイアウトと経路**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineAdjustTo] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LineAdjustTo  <br/> |
   
プログラムから、インデックスによって [LineAdjustTo] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOLineAdjustTo** <br/> |
   

