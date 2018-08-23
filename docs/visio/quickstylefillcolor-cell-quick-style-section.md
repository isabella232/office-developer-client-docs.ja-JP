---
title: '[QuickStyleFillColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: 0 ~ 7 の整数として、図形の塗りつぶしを使用するテーマの色を決定します。
ms.openlocfilehash: dcbb974947821327e7cff6634fd9435f5e5845bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806138"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a>[QuickStyleFillColor] セル ([クイック スタイル] セクション)

0 ~ 7 の整数として、図形の塗りつぶしを使用するテーマの色を決定します。
  
|||
|:-----|:-----|
|値  <br/> |説明  <br/> |
|0  <br/> |図形の塗りつぶしの色は、[ダーク] テーマの色を継承します。  <br/> |
|1  <br/> |図形の塗りつぶしの色は、[ライト] テーマの色を継承します。  <br/> |
|2  <br/> |図形の塗りつぶしの色は、[アクセント 1] テーマの色を継承します  <br/> |
|3  <br/> |図形の塗りつぶしの色は、[アクセント 2] テーマの色を継承します  <br/> |
|4  <br/> |図形の塗りつぶしの色は、[アクセント 3] テーマの色を継承します  <br/> |
|5  <br/> |図形の塗りつぶしの色は、[アクセント 4] テーマの色を継承します  <br/> |
|6  <br/> |図形の塗りつぶしの色は、[アクセント 5] テーマの色を継承します  <br/> |
|7  <br/> |図形の塗りつぶしの色は、[アクセント 6] テーマの色を継承します  <br/> |
   
## <a name="remarks"></a>Remarks

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleFillColor**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | QuickStyleFillColor  <br/> |
   
プログラムから、インデックスによって [**QuickStyleFillColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleFillColor** <br/> |
   

