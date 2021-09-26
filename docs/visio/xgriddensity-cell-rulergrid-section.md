---
title: '[XGridDensity] セル (Ruler &amp; Grid セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
ms.localizationpriority: medium
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: 使用する水平方向のグリッドの種類を指定します。
ms.openlocfilehash: ef2e65acde1121c1c4e822697867bf5a17d9102f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597717"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>[XGridDensity] セル (Ruler &amp; Grid セクション)

使用する水平方向のグリッドの種類を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visGridFixed** <br/> |
|2  <br/> |粗い  <br/> |**visGridCoarse** <br/> |
|4   <br/> |標準 (既定値)  <br/> |**visGridNormal** <br/> |
|8   <br/> |いい  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>注釈

このセルは、[ルーラーグリッド] ダイアログ ボックスの水平方向の [グリッド間隔] オプションに対応します ([表示] タブの [表示] 矢印を **クリック** します)。 **&amp;** 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XGridDensity] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |XGridDensity  <br/> |
   
プログラムから、インデックスによって [XGridDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visXGridDensity** <br/> |
   

