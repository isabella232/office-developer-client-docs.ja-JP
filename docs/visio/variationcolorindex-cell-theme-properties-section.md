---
title: '[VariationColorIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea95a90c-4729-4689-a6f4-31dfccf37b9b
description: ページ上のアクティブなテーマのバリエーションの色のインデックスを整数で指定します。
ms.openlocfilehash: 7582b779fb5be6bdf3528da137b1b08b8cd9c01a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355882"
---
# <a name="variationcolorindex-cell-theme-properties-section"></a>[VariationColorIndex] セル ([テーマのプロパティ] セクション)

ページ上のアクティブなテーマのバリエーションの色のインデックスを整数で指定します。
  
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[variationcolorindex]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [variationcolorindex]  <br/> |
   
プログラムから、インデックスによって [ **[variationcolorindex]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowThemeProperties** <br/> |
| セル インデックス:  <br/> |**visVariationColorIndex** <br/> |
   

