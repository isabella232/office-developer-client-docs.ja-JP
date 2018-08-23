---
title: '[TextDirection] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: テキスト ブロック内にある文字の方向を指定します。
ms.openlocfilehash: c238b6b2a47c968809869f8eb3e38b6f0db1dcad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806644"
---
# <a name="textdirection-cell-text-block-format-section"></a>[TextDirection] セル ([テキスト ブロックの書式設定] セクション)

テキスト ブロック内にある文字の方向を指定します。
  
|**値**|**Direction**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 横書き  <br/> |**visTxtBlkLeftToRight** <br/> |
| 1  <br/> | 縦書き  <br/> |**visTxtBlkTopToBottom** <br/> |
   
## <a name="remarks"></a>備考

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
   

