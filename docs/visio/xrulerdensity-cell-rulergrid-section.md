---
title: XRulerDensity セル (ルーラー&amp;グリッド セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: ページのルーラーに対して、水平方向の小区分を指定します。
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806813"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>XRulerDensity セル (ルーラー&amp;グリッド セクション)

ページのルーラーに対して、水平方向の小区分を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |固定  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |粗い  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |標準 (既定値)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |細かい  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>備考

このセルの水平方向の**目盛り**オプションに対応して、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[XRulerDensity] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |XRulerDensity  <br/> |
   
プログラムから、インデックスによって [XRulerDensity] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visXRulerDensity** <br/> |
   

