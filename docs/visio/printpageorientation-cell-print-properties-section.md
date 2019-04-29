---
title: '[PrintPageOrientation] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: ページの印刷方向を、縦向きにするか横向きにするかを指定します。
ms.openlocfilehash: f7e73bea5120d878a1b2dbf553a66b349d247fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434866"
---
# <a name="printpageorientation-cell-print-properties-section"></a>[PrintPageOrientation] セル ([Print Properties] セクション)

ページの印刷方向を、縦向きにするか横向きにするかを指定します。
  
|**値**|**Orientation**|**オートメーション定数**|
|:-----|:-----|:-----|
| .0  <br/> | プリンターの用紙サイズに合わせます。  <br/> |**vispposameasprinter** <br/> |
| 1   <br/> | Portrait  <br/> |**visppoportrait** <br/> |
|2   <br/> |写真  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>注釈

文書に新しいページを挿入すると、この設定は作業中のページの設定に既定値として設定されます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PrintPageOrientation] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [printpageorientation]  <br/> |
   
プログラムから、インデックスによって [PrintPageOrientation] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesPageOrientation** <br/> |
   

