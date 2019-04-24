---
title: '[SortKey] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: ショートカット メニューに表示されるハイパーリンクの順序を特定する数です。
ms.openlocfilehash: 002ab036f5305aa6daa631c15b0e9eb6148a9635
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335218"
---
# <a name="sortkey-cell-hyperlinks-section"></a>[SortKey] セル ([Hyperlinks] セクション)

ショートカット メニューに表示されるハイパーリンクの順序を特定する数です。
  
## <a name="remarks"></a>解説

ショートカット メニューのハイパーリンクは、昇順にソートされてメニューに表示されます。メニューの一番上には、最小の数値が表示されます。2 つのハイパーリンク行の [SortKey] セルの値が同じ場合、順番は物理的な行順序によって特定されます。既定値は 0 (ゼロ) です。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SortKey] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ハイパーリンク *名前*です。SortKey (ハイパーリンク** ) の行名  <br/> |
   
プログラムから、インデックスによって [SortKey] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
|行インデックス:  <br/> |**visRow1stHyperlink** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**vishlinksortkey** <br/> |
   

