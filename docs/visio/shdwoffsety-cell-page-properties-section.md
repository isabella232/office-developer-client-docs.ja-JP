---
title: '[ShdwOffsetY] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: 図形の影を図形から垂直方向にオフセットする場合の距離を、ページの単位で指定します。
ms.openlocfilehash: 0228fef00230dd1517d20067fda855225cef5533
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806473"
---
# <a name="shdwoffsety-cell-page-properties-section"></a>[ShdwOffsetY] セル ([Page Properties] セクション)

図形の影を図形から垂直方向にオフセットする場合の距離を、ページの単位で指定します。
  
## <a name="remarks"></a>注釈

この設定は、[**ページ設定**] ダイアログ ボックスで ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。 この値は、図面の縮尺に依存しません。 図面縮尺を変更して、影のオフセットは変わりません。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShdwOffsetY] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShdwOffsetY  <br/> |
   
プログラムから、インデックスによって [ShdwOffsetY] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageShdwOffsetY** <br/> |
   

