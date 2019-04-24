---
title: '[QuickStyleFillColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: 図形の塗りつぶしに使用するテーマの色を、0から7の整数で指定します。
ms.openlocfilehash: 3ace0de7e3bfc878a2101eaca3847ef079b8f919
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358727"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a>[QuickStyleFillColor] セル ([クイック スタイル] セクション)

図形の塗りつぶしに使用するテーマの色を、0から7の整数で指定します。
  
|||
|:-----|:-----|
|値  <br/> |説明  <br/> |
|.0  <br/> |図形の塗りつぶしの色は、[ダーク] テーマの色を継承します。  <br/> |
|1-d  <br/> |図形の塗りつぶしの色は、[ライト] テーマの色を継承します。  <br/> |
|pbm-2  <br/> |図形の塗りつぶしの色は、[アクセント 1] テーマの色を継承します  <br/> |
|1/3  <br/> |図形の塗りつぶしの色は、[アクセント 2] テーマの色を継承します  <br/> |
|2/4  <br/> |図形の塗りつぶしの色は、[アクセント 3] テーマの色を継承します  <br/> |
|5  <br/> |図形の塗りつぶしの色は、[アクセント 4] テーマの色を継承します  <br/> |
|シックス  <br/> |図形の塗りつぶしの色は、[アクセント 5] テーマの色を継承します  <br/> |
|7  <br/> |図形の塗りつぶしの色は、[アクセント 6] テーマの色を継承します  <br/> |
   
## <a name="remarks"></a>解説

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleFillColor**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [quickstylefillcolor]  <br/> |
   
プログラムから、インデックスによって [**QuickStyleFillColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleFillColor** <br/> |
   

