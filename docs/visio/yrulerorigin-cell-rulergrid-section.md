---
title: '[YRulerOrigin] セル (Ruler &amp; Grid セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1220
localization_priority: Normal
ms.assetid: 5d21b64f-a559-76ef-06df-d24c048cc6ef
description: ページの y 軸のルーラーに対して、ゼロ点を指定します。
ms.openlocfilehash: ead9ca453bfeb86f32a943950b297b9b629de95d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420417"
---
# <a name="yrulerorigin-cell-ruler-amp-grid-section"></a>[YRulerOrigin] セル (Ruler &amp; Grid セクション)

ページの y 軸のルーラーに対して、ゼロ点を指定します。
  
## <a name="remarks"></a>注釈

このセルは、[ルーラー グリッド] ダイアログ ボックスの垂直ルーラー **0** オプションに対応します ([表示] タブの [表示] 矢印を **クリック** します)。 **&amp;**  
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YRulerOrigin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |YRulerOrigin  <br/> |
   
プログラムから、インデックスによって [YRulerOrigin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visYRulerOrigin** <br/> |
   

