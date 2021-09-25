---
title: '[ColorSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fb84f71e-59c4-43d4-a28b-c3d6f267d2ae
description: 図形の配色が後に続くテーマのインデックスを整数で指定します。
ms.openlocfilehash: 92fb1ea57002496ca61e3bd38c5cf9d9b3edac65
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586678"
---
# <a name="colorschemeindex-cell-theme-properties-section"></a>[ColorSchemeIndex] セル ([テーマのプロパティ] セクション)

図形の配色が後に続くテーマのインデックスを整数で指定します。
  
## <a name="remarks"></a>注釈

別の数式 **、Cell** 要素の **N** 属性の値、または **CellsU** プロパティを使用するプログラムから、名前によって **ColorSchemeIndex** セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ColorSchemeIndex  <br/> |
   
プログラムからインデックスによって **ColorSchemeIndex** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowThemeProperties** <br/> |
| セル インデックス:  <br/> |**visColorSchemeIndex** <br/> |
   

