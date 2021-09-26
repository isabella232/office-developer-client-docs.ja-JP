---
title: '[YGridSpacing] セル (Ruler &amp; Grid セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1210
ms.localizationpriority: medium
ms.assetid: 30766e13-c90d-62fc-9c98-35ad7b0b4056
description: 固定グリッド (YGridDensity = 0) の垂直線の間隔を指定します。
ms.openlocfilehash: 0e031f8fd54ef8ce9e52cd2ee09afbbd452cfc53
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597696"
---
# <a name="ygridspacing-cell-ruler-amp-grid-section"></a>[YGridSpacing] セル (Ruler &amp; Grid セクション)

固定グリッド (YGridDensity = 0) の垂直線の間隔を指定します。
  
## <a name="remarks"></a>注釈

[ルーラー グリッド **] ダイアログ** ボックスの [垂直方向の最小間隔] オプション **に対応します &amp;**([表示] タブの [表示] 矢印を **クリック** します)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YGridSpacing] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |YGridSpacing  <br/> |
   
プログラムから、インデックスによって [YGridSpacing] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visYGridSpacing** <br/> |
   

