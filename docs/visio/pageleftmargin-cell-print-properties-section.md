---
title: '[PageLeftMargin] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
ms.localizationpriority: medium
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: 印刷ページの左余白を指定します。
ms.openlocfilehash: 0a7c5c9a19d14873bc134ffc47a7fe3c796b5993
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608131"
---
# <a name="pageleftmargin-cell-print-properties-section"></a>[PageLeftMargin] セル ([Print Properties] セクション)

印刷ページの左余白を指定します。
  
## <a name="remarks"></a>注釈

この値は物理単位を表し、縮尺または図面の単位には影響されません。たとえば、このセルの値が 0.25 インチなら、ページ単位がフィートの場合でも、この余白は 0.25 インチです。単位が明示されていない場合、既定ではこの値にページ単位が使用されます。 
  
別の数式または **CellsU** を使用したプログラムから、名前による [PageLeftMargin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | PageLeftMargin  <br/> |
   
プログラムから、インデックスによる [PageLeftMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPrintProperties** <br/> |
| セル インデックス:  <br/> |**visPrintPropertiesLeftMargin** <br/> |
   

