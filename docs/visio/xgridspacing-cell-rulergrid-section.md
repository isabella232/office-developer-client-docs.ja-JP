---
title: '[XGridSpacing] セル (Ruler &amp; Grid セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
ms.localizationpriority: medium
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: 固定グリッド (XGridDensity = 0) の水平線の間隔を指定します。
ms.openlocfilehash: 5c1dcf106c6b4124587d0b13d04f2ccf6e3a4f57
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603173"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a>[XGridSpacing] セル (Ruler &amp; Grid セクション)

固定グリッド (XGridDensity = 0) の水平線の間隔を指定します。
  
## <a name="remarks"></a>注釈

このセルは、[ルーラーグリッド] ダイアログ ボックスの水平方向の [最小間隔] オプションに対応します ([表示] タブの [表示] 矢印を **クリック** します)。 **&amp;** 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XGridSpacing] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |XGridSpacing  <br/> |
   
プログラムから、インデックスによって [XGridSpacing] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visXGridSpacing** <br/> |
   

