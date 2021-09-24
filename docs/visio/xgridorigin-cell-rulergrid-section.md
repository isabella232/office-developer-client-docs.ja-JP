---
title: '[XGridOrigin] セル ([Ruler &amp; Grid] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1155
ms.localizationpriority: medium
ms.assetid: 2b1a8902-b1d4-c3d9-8c9f-1a28fddacc59
description: グリッド原点の水平方向の座標を指定します。
ms.openlocfilehash: 0747152b2b5c3040df7233ab2a15a70d5fd8a1e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549295"
---
# <a name="xgridorigin-cell-ruler-amp-grid-section"></a>[XGridOrigin] セル ([Ruler &amp; Grid] セクション)

グリッド原点の水平方向の座標を指定します。
  
## <a name="remarks"></a>注釈

このセルは、[ルーラーグリッド] ダイアログ ボックスの水平グリッド原点オプションに対応します ([表示] タブの [表示] 矢印を **クリック** します)。 **&amp;** 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XGridOrigin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |XGridOrigin  <br/> |
   
プログラムから、インデックスによって [XGridOrigin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visXGridOrigin** <br/> |
   

