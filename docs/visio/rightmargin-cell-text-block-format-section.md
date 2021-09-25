---
title: '[RightMargin] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
ms.localizationpriority: medium
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: テキスト ブロックの右の枠線と、そのブロックに含まれるテキストとの間隔を指定します。既定値は 0.1 インチです。
ms.openlocfilehash: 4152c76a1950c598cbd979209d7a9967d11ce170
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559641"
---
# <a name="rightmargin-cell-text-block-format-section"></a>[RightMargin] セル ([Text Block Format] セクション)

テキスト ブロックの右の枠線と、そのブロックに含まれるテキストとの間隔を指定します。既定値は 0.1 インチです。
  
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
   

