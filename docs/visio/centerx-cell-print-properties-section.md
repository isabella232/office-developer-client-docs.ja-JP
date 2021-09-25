---
title: '[CenterX] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
ms.localizationpriority: medium
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: 図面ページをプリンター ページの左右の中央に揃えるかどうかを指定します。
ms.openlocfilehash: 5ea835ecd56a00c2697ed77e0dc2ca1559d21ba7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594797"
---
# <a name="centerx-cell-print-properties-section"></a>[CenterX] セル ([Print Properties] セクション)

図面ページをプリンター ページの左右の中央に揃えるかどうかを指定します。 
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図面ページをプリンター ページの左右の中央に揃えます。  <br/> |
| FALSE  <br/> | 図面ページをプリンター ページの左右の中央に揃えません (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

既定では、図面ページはプリンター ページの上と左に揃えられます。[CenterX] セルと [CenterY] セルを TRUE に設定すると、図面ページはプリンター ページの中央 (並べて表示する必要がある場合は複数ページの中央) に揃えられます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [CenterX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | CenterX  <br/> |
   
プログラムから、インデックスによって [CenterX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesCenterX** <br/> |
   

