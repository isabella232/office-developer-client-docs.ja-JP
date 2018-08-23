---
title: '[YRulerDensity] セル ([ルーラーとグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: ページのルーラーに対して、垂直方向の小区分を指定します。
ms.openlocfilehash: 4b5dcba7a5cb1a588f742b1c2ea6b430cb2af12c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806845"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>[YRulerDensity] セル ([ルーラーとグリッド] セクション)

ページのルーラーに対して、垂直方向の小区分を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |固定  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |粗い  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |標準 (既定値)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |細かい  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>注釈

このセル内の垂直方向の**目盛り**] オプションに対応して、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YRulerDensity] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |YRulerDensity  <br/> |
   
プログラムから、インデックスによって [YRulerDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visYRulerDensity** <br/> |
   

