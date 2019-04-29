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
ms.openlocfilehash: 4e1213990877e1260cc8cecd5a55beda4592a844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431009"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>[PageLineJumpDirX] セル ([Page Layout] セクション)

図面ページ上にある水平方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。
  
|**値**|**飛び越し点の方向**|**オートメーション定数**|
|:-----|:-----|:-----|
| .0  <br/> | 既定値です。左、またはページの設定に従います。  <br/> |**visLOJumpDirXDefault** <br/> |
| 1   <br/> | 上  <br/> |**visLOJumpDirXUp** <br/> |
| 2   <br/> | 下へ  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前による [PageLineJumpDirX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [pagelinejumpdirx]  <br/> |
   
プログラムから、インデックスによる [PageLineJumpDirX] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOJumpDirX** <br/> |
   

