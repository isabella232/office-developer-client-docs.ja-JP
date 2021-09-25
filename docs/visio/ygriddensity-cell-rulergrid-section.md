---
title: '[YGridDensity] セル (Ruler &amp; Grid セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
ms.localizationpriority: medium
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: 使用する垂直方向のグリッドの種類を指定します。
ms.openlocfilehash: 71b592831e6b84ea8ac7ad142ae5ad1b4c475a0e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553537"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>[YGridDensity] セル (Ruler &amp; Grid セクション)

使用する垂直方向のグリッドの種類を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visGridFixed** <br/> |
|2  <br/> |粗い  <br/> |**visGridCoarse** <br/> |
|4   <br/> |標準 (既定値)  <br/> |**visGridNormal** <br/> |
|8   <br/> |いい  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>注釈

このセルは、[ルーラーグリッド] ダイアログ ボックスの [垂直グリッド間隔] オプションに対応します ([表示] タブの [表示] 矢印を **クリック** します)。 **&amp;** 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YGridDensity] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |YGridDensity  <br/> |
   
プログラムから、インデックスによって [YGridDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visYGridDensity** <br/> |
   

