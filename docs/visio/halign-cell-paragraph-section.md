---
title: '[HAlign] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: 図形のテキスト ブロックにあるテキストの水平方向の配置を指定します。
ms.openlocfilehash: 224e495e8aea70c418a0ab7f5a7d56975d9868e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805516"
---
# <a name="halign-cell-paragraph-section"></a>[HAlign] セル ([段落] セクション)

図形のテキスト ブロックにあるテキストの水平方向の配置を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 左揃え  <br/> |**visHorzLeft** <br/> |
| 1  <br/> | 中央揃え  <br/> |**visHorzCenter** <br/> |
| 2  <br/> | 右揃え  <br/> |**visHorzRight** <br/> |
| 3  <br/> | 両端揃え  <br/> |**visHorzJustify** <br/> |
| 4  <br/> | 均等割付  <br/> |**visHorzForce** <br/> |
   
## <a name="remarks"></a>備考

両端揃えの場合、段落の最終行以外の各行の単語間に空白が挿入されて、テキストの左右の両端が余白に合わせて揃えられます
  
均等割付の場合は、段落の最終行も含めて、すべての行の両端を揃えます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [HAlign] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Para.HorzAlign [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [HAlign] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visHorzAlign** <br/> |
   

