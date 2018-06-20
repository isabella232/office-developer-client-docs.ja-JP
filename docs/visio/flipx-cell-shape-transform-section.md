---
title: '[FlipX] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251197
localization_priority: Normal
ms.assetid: 8d4f5e14-4f17-05a6-4092-5a102c9dc85f
description: 図形が左右反転されているかを示します。
ms.openlocfilehash: fc014ff6c5a3650361d6afd478a5858f84fb5c47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805412"
---
# <a name="flipx-cell-shape-transform-section"></a>[FlipX] セル ([Shape Transform] セクション)

図形が左右反転されているかを示します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形は左右反転されています。  <br/> |
| FALSE  <br/> | 図形は左右反転されていません。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [flipx] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Flipx]  <br/> |
   
プログラムから、インデックスによって [flipx] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowXFormOut** <br/> |
| セル インデックス:  <br/> |**visXFormFlipX** <br/> |
   

