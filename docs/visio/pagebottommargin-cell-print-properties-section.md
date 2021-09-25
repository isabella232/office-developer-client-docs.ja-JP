---
title: '[PageBottomMargin] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
ms.localizationpriority: medium
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: 印刷ページの下余白を指定します。
ms.openlocfilehash: 32e411b476bdd943e2294b7ba9943653ff0ce41c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577802"
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
   

