---
title: '[LeftMargin] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
localization_priority: Normal
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: テキスト ブロックの左枠からそのブロックに含まれるテキストまでの距離を指定します。既定値は 0.1 インチです。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、左余白の長さは変わりません。
ms.openlocfilehash: fee8eca8b5730e40518babe0c76549e10bebd902
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359389"
---
# <a name="leftmargin-cell-text-block-format-section"></a>[LeftMargin] セル ([Text Block Format] セクション)

テキスト ブロックの左枠からそのブロックに含まれるテキストまでの距離を指定します。既定値は 0.1 インチです。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、左余白の長さは変わりません。
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LeftMargin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LeftMargin  <br/> |
   
プログラムから、インデックスによって [LeftMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowText** <br/> |
| セル インデックス:  <br/> |**visTxtBlkLeftMargin** <br/> |
   

