---
title: '[CenterY] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
ms.localizationpriority: medium
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: 図面ページをプリンター ページの上下の中央に揃えるかどうかを指定します。
ms.openlocfilehash: b72acb3db2a56ab44da92dd30a3f748941ca7fbe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578026"
---
# <a name="centery-cell-print-properties-section"></a>[CenterY] セル ([Print Properties] セクション)

図面ページをプリンター ページの上下の中央に揃えるかどうかを指定します。 
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図面ページをプリンター ページの上下の中央に揃えます。  <br/> |
| FALSE  <br/> | 図面ページをプリンター ページの上下の中央に揃えません (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

既定では、図面ページはプリンター ページの上と左に揃えられます。[CenterX] セルと [CenterY] セルを TRUE に設定すると、図面ページはプリンター ページの中央 (並べて表示する必要がある場合は複数ページの中央) に揃えられます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [CenterY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | CenterY  <br/> |
   
プログラムから、インデックスによって [CenterY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesCenterY** <br/> |
   

