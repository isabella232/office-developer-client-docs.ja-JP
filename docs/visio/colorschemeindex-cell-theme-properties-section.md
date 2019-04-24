---
title: '[ColorSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb84f71e-59c4-43d4-a28b-c3d6f267d2ae
description: 図形の配色が後にかかるテーマのインデックスを整数で指定します。
ms.openlocfilehash: d67363b48454a717914b8ff9e39952609d848118
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357100"
---
# <a name="colorschemeindex-cell-theme-properties-section"></a>[ColorSchemeIndex] セル ([テーマのプロパティ] セクション)

図形の配色が後にかかるテーマのインデックスを整数で指定します。
  
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[colorschemeindex]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [colorschemeindex]  <br/> |
   
プログラムから、インデックスによって [ **[colorschemeindex]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowThemeProperties** <br/> |
| セル インデックス:  <br/> |**visColorSchemeIndex** <br/> |
   

