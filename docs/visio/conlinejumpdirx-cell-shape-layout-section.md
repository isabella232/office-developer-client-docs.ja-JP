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
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342750"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>[ConLineJumpDirX] セル ([Shape Layout] セクション)

図形に接続する水平方向の動的コネクタに表示される飛び越し点の向きを指定します。
  
|**値**|**飛び越し点の方向**|**オートメーション定数**|
|:-----|:-----|:-----|
| .0  <br/> | ページの既定値  <br/> |**visLOJumpDirXDefault** <br/> |
| 1-d  <br/> | 上  <br/> |**visLOJumpDirXUp** <br/> |
| pbm-2  <br/> | 下へ  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>解説

ページ上の*すべて*のコネクタジャンプの既定の水平方向を設定するには、[ページレイアウト] セクションの [[pagelinejumpdirx]] セルを使用します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineJumpDirX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [conlinejumpdirx]  <br/> |
   
プログラムから、インデックスによって [ConLineJumpDirX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowShapeLayout** <br/> |
| セル インデックス:  <br/> |**visSLOJumpDirX** <br/> |
   

