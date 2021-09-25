---
title: '[YRulerDensity] セル (Ruler &amp; Grid セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
ms.localizationpriority: medium
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: ページのルーラーに対して、垂直方向の小区分を指定します。
ms.openlocfilehash: 4e6085b08785f34758b33ee2d49a2f64146baa68
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553544"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>[YRulerDensity] セル (Ruler &amp; Grid セクション)

ページのルーラーに対して、垂直方向の小区分を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visRulerFixed** <br/> |
|8 ( &amp; H8)  <br/> |粗い  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |標準 (既定値)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |いい  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>注釈

このセルは、[ルーラーグリッド] ダイアログ ボックスの [垂直サブディビジョン]オプションに対応します ([表示] タブの [表示] 矢印を **クリック** します)。 **&amp;** 
  
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
   

