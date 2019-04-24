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
ms.openlocfilehash: be7ec4cccd53cc9d74811e2e45122c8bc29497d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349057"
---
# <a name="shdwoffsety-cell-page-properties-section"></a>[ShdwOffsetY] セル ([Page Properties] セクション)

図形の影を図形から垂直方向にオフセットする場合の距離を、ページの単位で指定します。
  
## <a name="remarks"></a>解説

この値は、[**ページ設定**] ダイアログ ボックスで設定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] 矢印をクリックします)。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、影のオフセットは変わりません。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwOffsetY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [shdwoffsety]  <br/> |
   
プログラムから、インデックスによって [ShdwOffsetY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageShdwOffsetY** <br/> |
   

