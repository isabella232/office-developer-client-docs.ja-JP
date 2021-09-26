---
title: '[WalkPreference] セル ([Glue Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
ms.localizationpriority: medium
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: 1-D 図形をあいまいな位置に移動したときに、その図形の端点が、動的接着によって接着先の図形にある水平方向の接続ポイントに移動するのか、または垂直方向の接続ポイントに移動するのかを指定します。既定では、1-D 図形の始点と終点の両方とも水平方向の接続ポイントに移動します。
ms.openlocfilehash: bd3b582ca00c8c4f9ef9018f219b0fdd9dafe07d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627115"
---
# <a name="walkpreference-cell-glue-info-section"></a>[WalkPreference] セル ([Glue Info] セクション)

1-D 図形をあいまいな位置に移動したときに、その図形の端点が、動的接着によって接着先の図形にある水平方向の接続ポイントに移動するのか、または垂直方向の接続ポイントに移動するのかを指定します。既定では、1-D 図形の始点と終点の両方とも水平方向の接続ポイントに移動します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 1  <br/> | 1-D 図形の始点は垂直方向の接続ポイントに移動し、終点は水平方向の接続ポイントに移動します (上から横または下から横の接続)。  <br/> |**visWalkPrefBegNS** <br/> |
| 2  <br/> | 1-D 図形の始点は水平方向の接続ポイントに移動し、終点は垂直方向の接続ポイントに移動します (横から上または横から下の接続)。  <br/> |**visWalkPrefEndNS** <br/> |
   
## <a name="remarks"></a>注釈

このセルは、動的コネクタには影響を与えません。動的コネクタの動作は、その迂回方法によって決まります。ページ上のすべての動的コネクタに対する既定の迂回方法については [RouteStyle] セルを、特定の動的コネクタの迂回方法については [ShapeRouteStyle] を参照してください。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [WalkPreference] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | WalkPreference  <br/> |
   
プログラムから、インデックスによって [WalkPreference] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visWalkPref** <br/> |
   

