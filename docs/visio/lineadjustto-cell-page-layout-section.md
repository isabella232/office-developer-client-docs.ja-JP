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
ms.openlocfilehash: 13540f9dc5e6e6861d3f3679bcf49204d553397a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805701"
---
# <a name="lineadjustto-cell-page-layout-section"></a>[LineAdjustTo] セル ([Page Layout] セクション)

線を束ねるときに対象とする動的コネクタを指定します。
  
|**値**|**調整**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |迂回方法の既定値に合わせる  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1  <br/> |近接しているすべての線  <br/> |**visPLOLineAdjustToAll** <br/> |
|2  <br/> |なし  <br/> |**visPLOLineAdjustToNone** <br/> |
|3  <br/> |関連付けられている線  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>備考

**[ページ設定**] ダイアログ ボックスで、[**レイアウトと経路**] タブで、このセルの値を設定することもできます ([**デザイン**] タブで、 **[ページ設定**の矢印をクリックし、[**レイアウトと経路**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineAdjustTo] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LineAdjustTo  <br/> |
   
プログラムから、インデックスによって [LineAdjustTo] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOLineAdjustTo** <br/> |
   

