---
title: '[PrintPageOrientation] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
ms.localizationpriority: medium
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: ページの印刷方向を、縦向きにするか横向きにするかを指定します。
ms.openlocfilehash: 7618077640875c9952a9c05e39ab1307407a3d91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570317"
---
# <a name="printpageorientation-cell-print-properties-section"></a>[PrintPageOrientation] セル ([Print Properties] セクション)

ページの印刷方向を、縦向きにするか横向きにするかを指定します。
  
|**値**|**Orientation**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | プリンターの用紙サイズに合わせます。  <br/> |**visPPOSameAsPrinter** <br/> |
| 1  <br/> | Portrait  <br/> |**visPPOPortrait** <br/> |
|2  <br/> |横向き  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>注釈

ドキュメントに新しいページを挿入すると、この設定は既定でアクティブ ページの設定になります。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PrintPageOrientation] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PrintPageOrientation  <br/> |
   
プログラムから、インデックスによって [PrintPageOrientation] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesPageOrientation** <br/> |
   

