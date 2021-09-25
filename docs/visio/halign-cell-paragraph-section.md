---
title: '[HAlign] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
ms.localizationpriority: medium
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: 図形のテキスト ブロックにあるテキストの水平方向の配置を指定します。
ms.openlocfilehash: 39f53eeeaed0225f7140f0ab164017d9dada7744
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570622"
---
# <a name="halign-cell-paragraph-section"></a>[HAlign] セル ([Paragraph] セクション)

図形のテキスト ブロックにあるテキストの水平方向の配置を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 左揃え  <br/> |**visHorzLeft** <br/> |
| 1  <br/> | 中央  <br/> |**visHorzCenter** <br/> |
| 2  <br/> | 右揃え  <br/> |**visHorzRight** <br/> |
| 3  <br/> | Justify  <br/> |**visHorzJustify** <br/> |
| 4   <br/> | 均等割付  <br/> |**visHorzForce** <br/> |
   
## <a name="remarks"></a>注釈

両端揃えの場合、段落の最終行以外の各行の単語間に空白が挿入されて、テキストの左右の両端が余白に合わせて揃えられます
  
均等割付の場合は、段落の最終行も含めて、すべての行の両端を揃えます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [HAlign] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Para.HorzAlign[ i ]*ここで**、i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [HAlign] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visHorzAlign** <br/> |
   

