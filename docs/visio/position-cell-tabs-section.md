---
title: '[Position] セル ([Tabs] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: タブ位置を指定します。タブ位置は図面の縮尺による影響を受けません。図面の縮尺を変更しても、タブ位置は変わりません。
ms.openlocfilehash: 06f3a9fd5cfdf78f5383e70f32f8514b0adab114
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806104"
---
# <a name="position-cell-tabs-section"></a>[Position] セル ([Tabs] セクション)

タブ位置を指定します。タブ位置は図面の縮尺による影響を受けません。図面の縮尺を変更しても、タブ位置は変わりません。
  
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって Position] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | タブします。  *ij* 、 *i*および*j* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Position] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTab** <br/> |
| 行インデックス:  <br/> |**visRowTab** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> | (*j* * 3) + **visTabPos** <br/> |
   

