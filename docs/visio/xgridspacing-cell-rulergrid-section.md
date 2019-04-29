---
title: '[xgridspacing] セル&amp; ([ルーラーグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: 固定グリッド (XGridDensity = 0) の水平線の間隔を指定します。
ms.openlocfilehash: 05b68a9721dbfc9c03402d384d976c42ef05b134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435076"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a>[xgridspacing] セル&amp; ([ルーラーグリッド] セクション)

固定グリッド (XGridDensity = 0) の水平線の間隔を指定します。
  
## <a name="remarks"></a>注釈

このセルは、[**ルーラー &amp;グリッド**] ダイアログボックス ([**表示**] タブの [**表示**] 矢印をクリックすると表示されます) の [上下の**間隔**] オプションに対応しています。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XGridSpacing] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[xgridspacing]  <br/> |
   
プログラムから、インデックスによって [XGridSpacing] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visXGridSpacing** <br/> |
   

