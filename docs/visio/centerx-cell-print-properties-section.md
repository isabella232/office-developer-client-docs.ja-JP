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
ms.openlocfilehash: 13b05ed71248a3f8fada947fca6b203c6ab19c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418079"
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
   

