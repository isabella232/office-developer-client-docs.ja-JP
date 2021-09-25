---
title: '[SpAfter] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
ms.localizationpriority: medium
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: 図形のテキスト ブロック内にある各段落の後に挿入する間隔を指定します。この値に、[SpLine] セルや [BottomMargin] セル (テキスト ブロックの最後の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。
ms.openlocfilehash: cdabd57f5dbad41e9b4d09e684c59df242d1e2ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622789"
---
# <a name="spafter-cell-paragraph-section"></a>[SpAfter] セル ([Paragraph] セクション)

図形のテキスト ブロック内にある各段落の後に挿入する間隔を指定します。この値に、[SpLine] セルや [BottomMargin] セル (テキスト ブロックの最後の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。
  
## <a name="remarks"></a>注釈

この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、[SpAfter] の設定は変わりません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SpAfter] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Para.SpAfter[  *i*  ]  *ここで、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [SpAfter] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス :  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス :  <br/> |**visSpaceAfter** <br/> |
   

