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
ms.openlocfilehash: 2adc7dadcb3702e6c5307bb569b2ae1df7aee54e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806115"
---
# <a name="printpageorientation-cell-print-properties-section"></a>[PrintPageOrientation] セル ([印刷のプロパティ] セクション)

ページの印刷方向を、縦向きにするか横向きにするかを指定します。
  
|**値**|**Orientation**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | プリンターの用紙サイズに合わせます。  <br/> |**visPPOSameAsPrinter** <br/> |
| 1  <br/> | 縦  <br/> |**visPPOPortrait** <br/> |
|2  <br/> |横  <br/> |**visPPOLandscape** <br/> |
   
## <a name="remarks"></a>注釈

ドキュメントに新しいページを挿入すると、この設定は既定で作業中のページで設定します。
  
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
   

