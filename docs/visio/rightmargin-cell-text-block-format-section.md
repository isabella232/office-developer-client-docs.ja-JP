---
title: '[RightMargin] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: テキスト ブロックの右の枠線と、そのブロックに含まれるテキストとの間隔を指定します。 既定値は 0.1 インチです。
ms.openlocfilehash: 7a9d2406792e9e57c6acd0e4291b624633e70dcb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433522"
---
# <a name="rightmargin-cell-text-block-format-section"></a>[RightMargin] セル ([Text Block Format] セクション)

テキスト ブロックの右の枠線と、そのブロックに含まれるテキストとの間隔を指定します。 既定値は 0.1 インチです。
  
## <a name="remarks"></a>注釈

この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、右余白は変わりません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [RightMargin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | RightMargin  <br/> |
   
プログラムから、インデックスによって [RightMargin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス :  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowText** <br/> |
| セル インデックス :  <br/> |**visTxtBlkRightMargin** <br/> |
   

