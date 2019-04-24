---
title: '[IndRight] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: 段落にあるテキストのすべての行について、テキスト ブロックの右余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、右インデントは変わりません。
ms.openlocfilehash: e6529bf41cb8fdd40371d9a663291961626afb56
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335344"
---
# <a name="indright-cell-paragraph-section"></a>[IndRight] セル ([Paragraph] セクション)

段落にあるテキストのすべての行について、テキスト ブロックの右余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、右インデントは変わりません。
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IndRight] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [indright] [ *i* ] *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [IndRight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visindentright** <br/> |
   

