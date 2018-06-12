---
title: '[CenterX] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: 図面ページをプリンター ページの左右の中央に揃えるかどうかを指定します。
ms.openlocfilehash: a12b60f7d183a27d938bd18a1f571ef01af455d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805001"
---
# <a name="centerx-cell-print-properties-section"></a>[CenterX] セル ([Print Properties] セクション)

図面ページをプリンター ページの左右の中央に揃えるかどうかを指定します。 
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図面ページをプリンター ページの左右の中央に揃えます。  <br/> |
| FALSE  <br/> | 図面ページをプリンター ページの左右の中央に揃えません (既定値)。  <br/> |
   
## <a name="remarks"></a>備考

既定では、図面ページはプリンター ページの上と左に揃えられます。[CenterX] セルと [CenterY] セルを TRUE に設定すると、図面ページはプリンター ページの中央 (並べて表示する必要がある場合は複数ページの中央) に揃えられます。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [centerx] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [Centerx]  <br/> |
   
プログラムから、インデックスによって [centerx] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesCenterX** <br/> |
   

