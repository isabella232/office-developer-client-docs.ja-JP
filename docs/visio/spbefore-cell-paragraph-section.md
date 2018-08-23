---
title: '[SpBefore] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: 図形のテキスト ブロック内にある各段落の前に挿入する間隔を指定します。この値に、[SpLine] セルや [TopMargin] セル (テキスト ブロックの最初の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。
ms.openlocfilehash: d33a10220499020ba1a1acedf5782fdb78925c07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806550"
---
# <a name="spbefore-cell-paragraph-section"></a>[SpBefore] セル ([段落] セクション)

図形のテキスト ブロック内にある各段落の前に挿入する間隔を指定します。この値に、[SpLine] セルや [TopMargin] セル (テキスト ブロックの最初の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。
  
## <a name="remarks"></a>備考

この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、[SpBefore] の設定は変わりません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SpBefore] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Para.SpBefore [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [SpBefore] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visSpaceBefore** <br/> |
   

