---
title: '[LineAdjustFrom] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: 複数の動的コネクタが迂回する場合に、線を分離するコネクタを指定します。
ms.openlocfilehash: ee3a107f7e19b53017c2ea24c94babceb49620d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805690"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a>[LineAdjustFrom] セル ([Page Layout] セクション)

複数の動的コネクタが迂回する場合に、線を分離するコネクタを指定します。
  
|**値**|**調整**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |関連付けられていない線  <br/> |**visPLOLineAdjustFromNotRelated** <br/> |
|1  <br/> |すべての線  <br/> |**visPLOLineAdjustFromAll** <br/> |
|2  <br/> |なし  <br/> |**visPLOLineAdjustFromNone** <br/> |
|3  <br/> |迂回方法の既定値に合わせる  <br/> |**visPLOLineAdjustFromRoutingDefault** <br/> |
   
## <a name="remarks"></a>備考

**[ページ設定**] ダイアログ ボックスで、[**レイアウトと経路**] タブで、このセルの値を設定することもできます ([**デザイン**] タブで、 **[ページ設定**の矢印をクリックし、[**レイアウトと経路**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineAdjustFrom] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LineAdjustFrom  <br/> |
   
プログラムから、インデックスによって [LineAdjustFrom] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOLineAdjustFrom** <br/> |
   

