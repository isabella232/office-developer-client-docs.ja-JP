---
title: '[XGridDensity] セル ([ルーラーとグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: 使用する水平方向のグリッドの種類を指定します。
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806817"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>[XGridDensity] セル ([ルーラーとグリッド] セクション)

使用する水平方向のグリッドの種類を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |固定  <br/> |**visGridFixed** <br/> |
|2  <br/> |粗い  <br/> |**visGridCoarse** <br/> |
|4  <br/> |標準 (既定値)  <br/> |**visGridNormal** <br/> |
|8  <br/> |細かい  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>注釈

このセルは、水平方向の**グリッド線の間隔**に対応するオプションで、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。 
  
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
   

