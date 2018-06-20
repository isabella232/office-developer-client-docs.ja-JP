---
title: '[BeginArrowSiz] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251629
localization_priority: Normal
ms.assetid: bfddb829-6e13-7d74-b9b9-2cb5c0937bae
description: 線の開始位置にある矢印のサイズを指定します。
ms.openlocfilehash: b38e4a0685fce6d7f4aea2192ed123665eacf40a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804796"
---
# <a name="beginarrowsize-cell-line-format-section"></a>[BeginArrowSiz] セル ([Line Format] セクション)

線の開始位置にある矢印のサイズを指定します。
  
|**値**|**Size**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 極小  <br/> |**visArrowSizeVerySmall** <br/> |
| 1  <br/> | 小  <br/> |**visArrowSizeSmall** <br/> |
| 2  <br/> | 中  <br/> |**visArrowSizeMedium** <br/> |
| 3  <br/> | 大  <br/> |**visArrowSizeLarge** <br/> |
| 4  <br/> | 特大  <br/> |**visArrowSizeVeryLarge** <br/> |
| 5  <br/> | 超特大  <br/> |**visArrowSizeJumbo** <br/> |
| 6  <br/> | 巨大  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>備考

**線**] ダイアログ ボックスで、矢印のサイズを設定することもできます。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[BeginArrowSize] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | BeginArrowSize  <br/> |
   
プログラムから、インデックスによって [BeginArrowSize] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLine** <br/> |
| セル インデックス:  <br/> |**visLineBeginArrowSize** <br/> |
   

