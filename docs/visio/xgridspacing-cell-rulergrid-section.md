---
title: XGridSpacing セル (ルーラー&amp;グリッド セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: 固定グリッド (XGridDensity = 0) の水平線の間隔を指定します。
ms.openlocfilehash: 5f461d02dae1574fe2b186b43166ef14d8251df2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806811"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a>XGridSpacing セル (ルーラー&amp;グリッド セクション)

固定グリッド (XGridDensity = 0) の水平線の間隔を指定します。
  
## <a name="remarks"></a>注釈

このセルは、水平方向の**最小間隔**に対応するオプションで、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[XGridSpacing] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |XGridSpacing  <br/> |
   
プログラムから、インデックスによって [XGridSpacing] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visXGridSpacing** <br/> |
   

