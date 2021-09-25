---
title: '[PageLineJumpDirX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
ms.localizationpriority: medium
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: 図面ページ上にある水平方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。
ms.openlocfilehash: ba5a76702a9aa6cb8e999c52edd3978259475061
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554300"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>[PageLineJumpDirX] セル ([Page Layout] セクション)

図面ページ上にある水平方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。
  
|**値**|**飛び越し点の方向**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 既定値です。左、またはページの設定に従います。  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | 上  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | 下へ  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前による [PageLineJumpDirX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | PageLineJumpDirX  <br/> |
   
プログラムから、インデックスによる [PageLineJumpDirX] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOJumpDirX** <br/> |
   

