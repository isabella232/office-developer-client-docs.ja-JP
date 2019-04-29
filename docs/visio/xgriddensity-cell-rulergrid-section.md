---
title: '[xgriddensity] セル&amp; ([ルーラーグリッド] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: 使用する水平方向のグリッドの種類を指定します。
ms.openlocfilehash: 5ebd172e56a66bfb39bd9bfa20967bb6b52c5aa2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436042"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>[xgriddensity] セル&amp; ([ルーラーグリッド] セクション)

使用する水平方向のグリッドの種類を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |Fixed  <br/> |**visGridFixed** <br/> |
|2   <br/> |粗い  <br/> |**visGridCoarse** <br/> |
|4   <br/> |標準 (既定値)  <br/> |**visGridNormal** <br/> |
|8   <br/> |いい  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>注釈

このセルは、[**ルーラー &amp;グリッド**] ダイアログボックスの [上下の**間隔**] オプションに対応しています ([**表示**] タブで [**表示**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XGridDensity] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |xgriddensity]  <br/> |
   
プログラムから、インデックスによって [XGridDensity] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visXGridDensity** <br/> |
   

