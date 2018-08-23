---
title: '[ConLineJumpDirX] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: 図形に接続する水平方向の動的コネクタに表示される飛び越し点の向きを指定します。
ms.openlocfilehash: 396830d0da22c15f036f95808b3a94c33e9dc5bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805081"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>[ConLineJumpDirX] セル ([図形レイアウト] セクション)

図形に接続する水平方向の動的コネクタに表示される飛び越し点の向きを指定します。
  
|**値**|**飛び越し点の方向**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | ページの既定値  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | 上  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | 下  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>注釈

ページにジャンプする*すべて*のコネクタの水平方向のデフォルトを設定するのには、PageLineJumpDirX セルを使用して、「ページ レイアウト」セクションでします。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineJumpDirX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ConLineJumpDirX  <br/> |
   
プログラムから、インデックスによって [ConLineJumpDirX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowShapeLayout** <br/> |
| セル インデックス:  <br/> |**visSLOJumpDirX** <br/> |
   

