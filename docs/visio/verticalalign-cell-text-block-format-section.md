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
ms.openlocfilehash: cfd34f17eec597c306b69f76929877013b39015e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806768"
---
# <a name="verticalalign-cell-text-block-format-section"></a>[VerticalAlign] セル ([Text Block Format] セクション)

テキスト ブロック内にあるテキストに対して、垂直方向の整列方法を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 上揃え  <br/> |**visVertTop** <br/> |
| 1  <br/> | 中央揃え  <br/> |**visVertMiddle** <br/> |
| 2  <br/> | 下揃え  <br/> |**visVertBottom** <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[VerticalAlign] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | VerticalAlign  <br/> |
   
プログラムから、インデックスによって [VerticalAlign] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowText** <br/> |
| セル インデックス:  <br/> |**visTxtBlkVerticalAlign** <br/> |
   

