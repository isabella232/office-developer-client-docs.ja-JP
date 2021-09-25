---
title: '[LineToNodeY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251650
ms.localizationpriority: medium
ms.assetid: 49d649e8-1603-192b-2984-e5d0b713da89
description: 図面ページにあるすべてのコネクタと図形間の垂直方向のクリアランスを指定します。
ms.openlocfilehash: 0d5bb760c28efb29e334a4aa822c5f94e066088c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574021"
---
# <a name="linetonodey-cell-page-layout-section"></a>[LineToNodeY] セル ([Page Layout] セクション)

図面ページにあるすべてのコネクタと図形間の垂直方向のクリアランスを指定します。
  
## <a name="remarks"></a>注釈

このセルの値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックし、[**レイアウトと経路**] をクリックして、[**間隔**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineToNodeY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LineToNodeY  <br/> |
   
プログラムから、インデックスによって [LineToNodeY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOLineToNodeY** <br/> |
   

