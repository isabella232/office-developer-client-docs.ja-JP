---
title: '[PageLineJumpDirX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: 図面ページ上にある水平方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。
ms.openlocfilehash: d414313e98107790f9236c0afabdc5747c6a2a10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805961"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>[PageLineJumpDirX] セル ([Page Layout] セクション)

図面ページ上にある水平方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。
  
|**値**|**線の飛び越し点の方向**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 既定値です。左、またはページの設定に従います。  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | 上  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | 下  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PageLineJumpDirX] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | PageLineJumpDirX  <br/> |
   
プログラムから、インデックスによって [PageLineJumpDirX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOJumpDirX** <br/> |
   

