---
title: '[ygridspacing] セル&amp; ([ルーラーグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1210
localization_priority: Normal
ms.assetid: 30766e13-c90d-62fc-9c98-35ad7b0b4056
description: 固定グリッド (YGridDensity = 0) の垂直線の間隔を指定します。
ms.openlocfilehash: fc355b4e509494e9e7570122a8a3a7a3ce2e0588
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283430"
---
# <a name="ygridspacing-cell-ruler-amp-grid-section"></a>[ygridspacing] セル&amp; ([ルーラーグリッド] セクション)

固定グリッド (YGridDensity = 0) の垂直線の間隔を指定します。
  
## <a name="remarks"></a>解説

[**ルーラー &amp;グリッド**] ダイアログボックスの [上下の**最小間隔**] オプションに対応します ([**表示**] タブで [**表示**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YGridSpacing] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[ygridspacing]  <br/> |
   
プログラムから、インデックスによって [YGridSpacing] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visygridspacing** <br/> |
   

