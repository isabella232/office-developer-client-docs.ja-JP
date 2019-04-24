---
title: '[yrulerdensity] セル&amp; ([ルーラーグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: ページのルーラーに対して、垂直方向の小区分を指定します。
ms.openlocfilehash: c92c48f6c86fc794cf6f53a87fdb99e67a73b9f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357205"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>[yrulerdensity] セル&amp; ([ルーラーグリッド] セクション)

ページのルーラーに対して、垂直方向の小区分を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |Fixed  <br/> |**visrulerfixed** <br/> |
|8 (&amp;H8)  <br/> |粗い  <br/> |**visrulercoarse** <br/> |
|16 (&amp;H10)  <br/> |標準 (既定値)  <br/> |**visrulernormal** <br/> |
|32 (&amp;H20)  <br/> |いい  <br/> |**visrulerfine** <br/> |
   
## <a name="remarks"></a>解説

このセルは、[**ルーラー &amp;グリッド**] ダイアログボックス ([**表示**] タブの [**表示**] 矢印をクリック) の [垂直方向の**目盛り**] オプションに対応しています。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [YRulerDensity] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[yrulerdensity]  <br/> |
   
プログラムから、インデックスによって [YRulerDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visyrulerdensity** <br/> |
   

