---
title: '[ConLineJumpDirY] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: 図形に接続する垂直方向の動的コネクタに表示される飛び越し点の向きを指定します。
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404772"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>[ConLineJumpDirY] セル ([Shape Layout] セクション)

図形に接続する垂直方向の動的コネクタに表示される飛び越し点の向きを指定します。
  
|**値**|**飛び越し点の方向**|**オートメーション定数**|
|:-----|:-----|:-----|
| .0  <br/> | ページの既定値  <br/> |**visLOJumpDirYDefault** <br/> |
| 1   <br/> | 左  <br/> |**visLOJumpDirYLeft** <br/> |
| 2   <br/> | 右  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>注釈

ページ上の*すべて*のコネクタジャンプの既定の垂直方向を設定するには、[ページレイアウト] セクションの [[pagelinejumpdiry]] セルを使用します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineJumpDirY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [conlinejumpdiry]  <br/> |
   
プログラムから、インデックスによって [ConLineJumpDirY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowShapeLayout** <br/> |
| セル インデックス:  <br/> |**visSLOJumpDirY** <br/> |
   

