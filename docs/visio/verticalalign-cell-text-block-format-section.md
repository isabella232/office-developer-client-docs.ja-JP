---
title: '[VerticalAlign] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
ms.localizationpriority: medium
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: テキスト ブロック内にあるテキストに対して、垂直方向の整列方法を指定します。
ms.openlocfilehash: 59892b4c28278bf59dbf474f900c0cf7e498dbd8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622642"
---
# <a name="verticalalign-cell-text-block-format-section"></a>[VerticalAlign] セル ([Text Block Format] セクション)

テキスト ブロック内にあるテキストに対して、垂直方向の整列方法を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | Top  <br/> |**visVertTop** <br/> |
| 1  <br/> | Middle  <br/> |**visVertMiddle** <br/> |
| 2  <br/> | Bottom  <br/> |**visVertBottom** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [VerticalAlign] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | VerticalAlign  <br/> |
   
プログラムから、インデックスによって [VerticalAlign] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowText** <br/> |
| セル インデックス:  <br/> |**visTxtBlkVerticalAlign** <br/> |
   

