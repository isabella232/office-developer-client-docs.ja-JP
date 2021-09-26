---
title: '[YGridOrigin] セル (Ruler &amp; Grid セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1205
ms.localizationpriority: medium
ms.assetid: eeec59f8-f301-5639-ffd6-8a36b2bf9c8f
description: グリッド原点の垂直方向の座標を指定します。
ms.openlocfilehash: 0a8bf07802c69319a79235a556ef46334cad2d37
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622586"
---
# <a name="ygridorigin-cell-ruler-amp-grid-section"></a>[YGridOrigin] セル (Ruler &amp; Grid セクション)

グリッド原点の垂直方向の座標を指定します。
  
## <a name="remarks"></a>注釈

このセルは、[ルーラーグリッド] ダイアログ ボックスの [垂直グリッド原点] オプションに対応します ([表示] タブの [表示] 矢印を **クリック** します)。 **&amp;** 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YGridOrigin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |YGridOrigin  <br/> |
   
プログラムから、インデックスによって [YGridOrigin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visYGridOrigin** <br/> |
   

