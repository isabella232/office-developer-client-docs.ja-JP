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
ms.openlocfilehash: 1663fac8efdf06599d1e3c00d5eb0d00ec52e476
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805966"
---
# <a name="pagesy-cell-print-properties-section"></a>[PagesY] セル ([Print Properties] セクション)

図面ページに上下を揃えるプリンター ページの番号を指定します。 
  
## <a name="remarks"></a>備考

この値は、[OnPage] セルが TRUE に設定されているときに限り使用されます。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [pagesy] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Pagesy]  <br/> |
   
プログラムから、インデックスによって [pagesy] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesPagesY** <br/> |
   

