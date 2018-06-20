---
title: '[ScaleY] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: '[プリンター] ページで、図面ページの表示倍率の割合を指定します。'
ms.openlocfilehash: 2735b2cfce04cc9a8d8da1a815081aaa5892c723
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806347"
---
# <a name="scaley-cell-print-properties-section"></a>[ScaleY] セル ([Print Properties] セクション)

[プリンター] ページで、図面ページの表示倍率の割合を指定します。
  
## <a name="remarks"></a>備考

[Onpage] セルの値が FALSE である場合にのみ、この値が使用されます。 ScaleX と ScaleY のセルは、同じ値が、[**ページ設定**] ダイアログ ボックスの [**印刷設定**] タブの **[拡大/縮小**設定の値に対応して常にある ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって scaley] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |Scaley]  <br/> |
   
プログラムから、インデックスによって [scaley] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesScaleY** <br/> |
   

