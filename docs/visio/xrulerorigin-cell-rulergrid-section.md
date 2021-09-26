---
title: '[XRulerOrigin] セル ([ルーラー &amp; グリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1170
ms.localizationpriority: medium
ms.assetid: 328f8ab5-217f-0336-0d56-611eff509fe8
description: ページの x 軸のルーラーに対して、ゼロ点を指定します。
ms.openlocfilehash: 5788094abad6cadc2b32f8a9fe9d7e2a80c4209b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622579"
---
# <a name="xrulerorigin-cell-ruler-amp-grid-section"></a>[XRulerOrigin] セル ([ルーラー &amp; グリッド] セクション)

ページの x 軸のルーラーに対して、ゼロ点を指定します。
  
## <a name="remarks"></a>注釈

このセルは、[ルーラー グリッド] ダイアログ ボックスの水平ルーラー **0** オプションに対応します ([表示] タブの [表示] 矢印を **クリック** します)。 **&amp;**  
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XRulerOrigin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |XRulerOrigin  <br/> |
   
プログラムから、インデックスによって [XRulerOrigin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visXRulerOrigin** <br/> |
   

