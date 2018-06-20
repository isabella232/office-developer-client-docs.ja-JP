---
title: '[LineToNodeY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251650
localization_priority: Normal
ms.assetid: 49d649e8-1603-192b-2984-e5d0b713da89
description: 図面ページにあるすべてのコネクタと図形間の垂直方向のクリアランスを指定します。
ms.openlocfilehash: bd5216a68abc4bcd8c3ef807b98280edb0ad29b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805717"
---
# <a name="linetonodey-cell-page-layout-section"></a>[LineToNodeY] セル ([Page Layout] セクション)

図面ページにあるすべてのコネクタと図形間の垂直方向のクリアランスを指定します。
  
## <a name="remarks"></a>注釈

**レイアウトと間隔**] ダイアログ ボックスで、このセルの値を設定することもできます。 ([**デザイン**] タブで、**ページ設定**の矢印をクリックして、[**レイアウトと経路**、および、[**間隔**] をクリックします。)
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineToNodeY] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LineToNodeY  <br/> |
   
プログラムから、インデックスによって [LineToNodeY] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOLineToNodeY** <br/> |
   

