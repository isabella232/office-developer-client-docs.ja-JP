---
title: '[ConLineJumpDirX] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
ms.localizationpriority: medium
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: 図形に接続する水平方向の動的コネクタに表示される飛び越し点の向きを指定します。
ms.openlocfilehash: 2749d1fde3ebcfa6cd5a1c367ea9ce8674925be5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608397"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>[ConLineJumpDirX] セル ([Shape Layout] セクション)

図形に接続する水平方向の動的コネクタに表示される飛び越し点の向きを指定します。
  
|**値**|**飛び越し点の方向**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | ページの既定値  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | 上  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | 下へ  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>注釈

ページ上のすべてのコネクタ ジャンプの既定の水平方向を設定するには、[ページ レイアウト] セクションの [PageLineJumpDirX] セルを使用します。 
  
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
   

