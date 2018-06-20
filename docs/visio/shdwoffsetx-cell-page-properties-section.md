---
title: '[ShdwOffsetX] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: 図形の影を図形から水平方向にオフセットする場合の距離を、ページの単位で指定します。
ms.openlocfilehash: 9aec108146e329d7a8161acc4ca7cdcb19424eff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806456"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a>[ShdwOffsetX] セル ([Page Properties] セクション)

図形の影を図形から水平方向にオフセットする場合の距離を、ページの単位で指定します。
  
## <a name="remarks"></a>注釈

この設定は、[**ページ設定**] ダイアログ ボックスで ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。 この値は、図面の縮尺に依存しません。 図面縮尺を変更して、影のオフセットは変わりません。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShdwOffsetX] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShdwOffsetX  <br/> |
   
プログラムから、インデックスによって [ShdwOffsetX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageShdwOffsetX** <br/> |
   

