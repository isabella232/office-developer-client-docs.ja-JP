---
title: '[PageLineJumpDirY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: 図面ページ上にある垂直方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。
ms.openlocfilehash: 640ad93fbccf2cec26bda535c288c881aea32207
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805972"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a>[PageLineJumpDirY] セル ([ページ レイアウト] セクション)

図面ページ上にある垂直方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。
  
|**値**|**飛び越し点の方向**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 既定値です。上、またはページの設定に従います。  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | 左  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | 右  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前による [PageLineJumpDirY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | PageLineJumpDirY  <br/> |
   
プログラムから、インデックスによる [PageLineJumpDirY] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOJumpDirY** <br/> |
   

