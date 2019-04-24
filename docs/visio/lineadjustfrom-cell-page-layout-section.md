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
ms.openlocfilehash: 3eb9f5513ee3ce2f5dce96cb47c356bca29a289c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359326"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a>[LineAdjustFrom] セル ([Page Layout] セクション)

複数の動的コネクタが迂回する場合に、線を分離するコネクタを指定します。
  
|**値**|**セレクター**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |関連付けられていない線  <br/> |**visPLOLineAdjustFromNotRelated** <br/> |
|1-d  <br/> |すべての線  <br/> |**visPLOLineAdjustFromAll** <br/> |
|pbm-2  <br/> |なし  <br/> |**visPLOLineAdjustFromNone** <br/> |
|1/3  <br/> |迂回方法の既定値に合わせる  <br/> |**visPLOLineAdjustFromRoutingDefault** <br/> |
   
## <a name="remarks"></a>解説

このセルの値は、[**ページ設定**] ダイアログ ボックスの [**レイアウトと経路**] タブで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックして、[**レイアウトと経路**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineAdjustFrom] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[lineadjustfrom]  <br/> |
   
プログラムから、インデックスによって [LineAdjustFrom] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOLineAdjustFrom** <br/> |
   

