---
title: '[PagesY] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
localization_priority: Normal
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: 図面ページに上下を揃えるプリンター ページの番号を指定します。
ms.openlocfilehash: 43d4081439525c516d3da28b6c0e46e9273d85c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339978"
---
# <a name="pagesy-cell-print-properties-section"></a>[PagesY] セル ([Print Properties] セクション)

図面ページに上下を揃えるプリンター ページの番号を指定します。 
  
## <a name="remarks"></a>解説

この値は、[OnPage] セルが TRUE に設定されているときに限り使用されます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PagesY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [pagesy]  <br/> |
   
プログラムから、インデックスによって [PagesY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesPagesY** <br/> |
   

