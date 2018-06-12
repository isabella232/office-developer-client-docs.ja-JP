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
description: テキスト ブロックの右の枠線と、そのブロックに含まれるテキストとの間隔を指定します。既定値は 0.1 インチです。
ms.openlocfilehash: 57fdb320395a9a6562983a0148b37c4a70a9a9b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806236"
---
# <a name="rightmargin-cell-text-block-format-section"></a>[RightMargin] セル ([Text Block Format] セクション)

テキスト ブロックの右の枠線と、そのブロックに含まれるテキストとの間隔を指定します。既定値は 0.1 インチです。
  
## <a name="remarks"></a>備考

この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、右余白は変わりません。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって RightMargin] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | 右マージン  <br/> |
   
プログラムから、インデックスによって [RightMargin] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowText** <br/> |
| セル インデックス:  <br/> |**visTxtBlkRightMargin** <br/> |
   

