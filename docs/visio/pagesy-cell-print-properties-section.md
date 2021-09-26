---
title: '[PagesY] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
ms.localizationpriority: medium
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: 図面ページに上下を揃えるプリンター ページの番号を指定します。
ms.openlocfilehash: 190cd49ff521a11c3daa70981bb17794a9a7b10b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627773"
---
# <a name="pagesy-cell-print-properties-section"></a>[PagesY] セル ([Print Properties] セクション)

図面ページに上下を揃えるプリンター ページの番号を指定します。 
  
## <a name="remarks"></a>注釈

この値は、[OnPage] セルが TRUE に設定されているときに限り使用されます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PagesY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PagesY  <br/> |
   
プログラムから、インデックスによって [PagesY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesPagesY** <br/> |
   

