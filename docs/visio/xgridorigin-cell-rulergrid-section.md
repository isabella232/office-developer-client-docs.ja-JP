---
title: '[xgridorigin] セル&amp; ([ルーラ Grid] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1155
localization_priority: Normal
ms.assetid: 2b1a8902-b1d4-c3d9-8c9f-1a28fddacc59
description: グリッド原点の水平方向の座標を指定します。
ms.openlocfilehash: ee58ea7d950dd7e422f8a60a13bac8aa4ed353a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428621"
---
# <a name="xgridorigin-cell-ruler-amp-grid-section"></a>[xgridorigin] セル&amp; ([ルーラ Grid] セクション)

グリッド原点の水平方向の座標を指定します。
  
## <a name="remarks"></a>注釈

このセルは、[**ルーラー &amp;グリッド**] ダイアログボックス ([**表示**] タブの [表示] 矢印をクリックすると**表示**されます) の [水平方向の**グリッド線**] オプションに対応しています。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XGridOrigin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[xgridorigin]  <br/> |
   
プログラムから、インデックスによって [XGridOrigin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visXGridOrigin** <br/> |
   

