---
title: YGridDensity セル (ルーラー&amp;グリッド セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: 使用する垂直方向のグリッドの種類を指定します。
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806847"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>YGridDensity セル (ルーラー&amp;グリッド セクション)

使用する垂直方向のグリッドの種類を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |固定  <br/> |**visGridFixed** <br/> |
|2  <br/> |粗い  <br/> |**visGridCoarse** <br/> |
|4  <br/> |標準 (既定値)  <br/> |**visGridNormal** <br/> |
|8  <br/> |細かい  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>備考

このセルは、垂直方向の**グリッド線の間隔**に対応するオプションで、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[YGridDensity] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |YGridDensity  <br/> |
   
プログラムから、インデックスによって [YGridDensity] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visYGridDensity** <br/> |
   

