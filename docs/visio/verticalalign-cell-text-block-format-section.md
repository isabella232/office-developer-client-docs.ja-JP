---
title: '[VerticalAlign] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: テキスト ブロック内にあるテキストに対して、垂直方向の整列方法を指定します。
ms.openlocfilehash: 954a0cf0b80d6b675dcc016997f1923041069eac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356142"
---
# <a name="verticalalign-cell-text-block-format-section"></a>[VerticalAlign] セル ([Text Block Format] セクション)

テキスト ブロック内にあるテキストに対して、垂直方向の整列方法を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| .0  <br/> | Top  <br/> |**visVertTop** <br/> |
| 1-d  <br/> | 区分  <br/> |**visVertMiddle** <br/> |
| pbm-2  <br/> | 下  <br/> |**visVertBottom** <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [VerticalAlign] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [verticalalign]  <br/> |
   
プログラムから、インデックスによって [VerticalAlign] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowText** <br/> |
| セル インデックス:  <br/> |**visTxtBlkVerticalAlign** <br/> |
   

