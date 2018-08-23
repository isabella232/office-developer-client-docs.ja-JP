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
ms.openlocfilehash: 2d0c0964b52c9afbccc9cb507024825434702b6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805069"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>[ConLineJumpDirY] セル ([図形レイアウト] セクション)

図形に接続する垂直方向の動的コネクタに表示される飛び越し点の向きを指定します。
  
|**値**|**線の飛び越し点の方向**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | ページの既定値  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | 左  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | 右  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>注釈

ページにジャンプする*すべて*のコネクタの垂直方向の既定値を設定するのには、PageLineJumpDirY セルを使用して、「ページ レイアウト」セクションでします。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineJumpDirY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ConLineJumpDirY  <br/> |
   
プログラムから、インデックスによって [ConLineJumpDirY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowShapeLayout** <br/> |
| セル インデックス:  <br/> |**visSLOJumpDirY** <br/> |
   

