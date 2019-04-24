---
title: '[PagesX] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60064
localization_priority: Normal
ms.assetid: a10bf4c2-24f4-4c53-39ba-2b8cd5b50d2c
description: 図面ページに左右を揃えるプリンター ページの番号を指定します。
ms.openlocfilehash: e912aef2277f5a7d2af5352897654ee986836c48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340139"
---
# <a name="pagesx-cell-print-properties-section"></a>[PagesX] セル ([Print Properties] セクション)

図面ページに左右を揃えるプリンター ページの番号を指定します。 
  
## <a name="remarks"></a>解説

この値は、[OnPage] セルが TRUE に設定されているときに限り使用されます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PagesX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [pagesx]  <br/> |
   
プログラムから、インデックスによって [PagesX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesPagesX** <br/> |
   

