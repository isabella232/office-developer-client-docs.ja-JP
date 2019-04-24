---
title: '[IndLeft] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: 段落にあるテキストのすべての行について、テキスト ブロックの左余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、左インデントは変わりません。
ms.openlocfilehash: 2a942ef3d874b8d1ce2ef85f423c93bc0db33230
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335337"
---
# <a name="indleft-cell-paragraph-section"></a>[IndLeft] セル ([Paragraph] セクション)

段落にあるテキストのすべての行について、テキスト ブロックの左余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、左インデントは変わりません。
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IndLeft] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | <1> 左 [ *i* ] ( *i* =, 2, 3...」を指定します。  <br/> |
   
プログラムから、インデックスによって [IndLeft] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visindentleft** <br/> |
   

