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
ms.openlocfilehash: fb67cf87f5e50719d24b0f354acc93209eed8811
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805952"
---
# <a name="pagebottommargin-cell-print-properties-section"></a>[PageBottomMargin] セル ([Print Properties] セクション)

印刷ページの下余白を指定します。
  
## <a name="remarks"></a>備考

この値は物理単位を表し、縮尺または図面の単位には影響されません。たとえば、このセルの値が 0.5 インチなら、ページ単位がフィートの場合でも、この余白は 0.5 インチです。単位が明示されていない場合、既定ではこの値にページ単位が使用されます。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PageBottomMargin] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | PageBottomMargin  <br/> |
   
プログラムから、インデックスによって [PageBottomMargin] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesBottomMargin** <br/> |
   

