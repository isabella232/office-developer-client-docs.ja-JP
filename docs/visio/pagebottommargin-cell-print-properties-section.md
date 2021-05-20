---
title: '[PageBottomMargin] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: 印刷ページの下余白を指定します。
ms.openlocfilehash: f546d89b8761c6c1b7340af69d2b48f16c180767
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438597"
---
# <a name="pagebottommargin-cell-print-properties-section"></a>[PageBottomMargin] セル ([Print Properties] セクション)

印刷ページの下余白を指定します。
  
## <a name="remarks"></a>注釈

この値は物理単位を表し、縮尺または図面の単位には影響されません。たとえば、このセルの値が 0.5 インチなら、ページ単位がフィートの場合でも、この余白は 0.5 インチです。単位が明示されていない場合、既定ではこの値にページ単位が使用されます。 
  
別の数式または **CellsU** を使用したプログラムから、名前による [PageBottomMargin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | PageBottomMargin  <br/> |
   
プログラムから、インデックスによる [PageBottomMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesBottomMargin** <br/> |
   

