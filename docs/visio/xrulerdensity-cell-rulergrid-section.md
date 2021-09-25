---
title: '[XRulerDensity] セル (Ruler &amp; Grid セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
ms.localizationpriority: medium
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: ページのルーラーに対して、水平方向の小区分を指定します。
ms.openlocfilehash: 23eacc8e1a99df92bf9cdb705adda6cb3ecad890
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603110"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>[XRulerDensity] セル (Ruler &amp; Grid セクション)

ページのルーラーに対して、水平方向の小区分を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visRulerFixed** <br/> |
|8 ( &amp; H8)  <br/> |粗い  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |標準 (既定値)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |いい  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>注釈

このセルは、[ルーラーグリッド] ダイアログ ボックスの水平方向の [サブディビジョン] オプションに対応します ([表示] タブの [表示] 矢印を **クリック** します)。 **&amp;** 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XRulerDensity] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |XRulerDensity  <br/> |
   
プログラムから、インデックスによって [XRulerDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visXRulerDensity** <br/> |
   

