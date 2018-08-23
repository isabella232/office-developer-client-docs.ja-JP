---
title: '[ScaleX] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: '[プリンター] ページで、図面ページの表示倍率の割合を指定します。'
ms.openlocfilehash: 1713e88f06dc93a2806e64cae3d7af20c9df1fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806351"
---
# <a name="scalex-cell-print-properties-section"></a>[ScaleX] セル ([印刷のプロパティ] セクション)

[プリンター] ページで、図面ページの表示倍率の割合を指定します。
  
## <a name="remarks"></a>注釈

[Onpage] セルの値が FALSE である場合にのみ、この値が使用されます。 ScaleX と ScaleY のセルは、同じ値が、[**ページ設定**] ダイアログ ボックスの [**印刷設定**] タブの **[拡大/縮小**設定の値に対応して常にある ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ScaleX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[Scalex]  <br/> |
   
プログラムから、インデックスによって [ScaleX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesScaleX** <br/> |
   

