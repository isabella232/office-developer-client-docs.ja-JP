---
title: '[TextDirection] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
ms.localizationpriority: medium
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: テキスト ブロック内にある文字の方向を指定します。
ms.openlocfilehash: d70cf6152fcb3e7ffbda69f6a6e6aaf758074fd1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553691"
---
# <a name="textdirection-cell-text-block-format-section"></a>[TextDirection] セル ([Text Block Format] セクション)

テキスト ブロック内にある文字の方向を指定します。
  
|**値**|**Direction**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 横方向  <br/> |**visTxtBlkLeftToRight** <br/> |
| 1  <br/> | 縦  <br/> |**visTxtBlkTopToBottom** <br/> |
   
## <a name="remarks"></a>注釈

Visio Version 5.0 日本語版では、このセルの値は [Miscellaneous] セクションの [VerticalText] セルに格納されていました。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TextDirection] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | TextDirection  <br/> |
   
プログラムから、インデックスによって [TextDirection] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowText** <br/> |
| セル インデックス:  <br/> |**visTxtBlkDirection** <br/> |
   

