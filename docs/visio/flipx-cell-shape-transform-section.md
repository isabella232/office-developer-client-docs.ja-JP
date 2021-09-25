---
title: '[FlipX] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251197
ms.localizationpriority: medium
ms.assetid: 8d4f5e14-4f17-05a6-4092-5a102c9dc85f
description: 図形が左右反転されているかを示します。
ms.openlocfilehash: 23dc298b00463da39b9345be59cf7d4267a636a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554804"
---
# <a name="flipx-cell-shape-transform-section"></a>[FlipX] セル ([Shape Transform] セクション)

図形が左右反転されているかを示します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形は左右反転されています。  <br/> |
| FALSE  <br/> | 図形は左右反転されていません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FlipX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | FlipX  <br/> |
   
プログラムから、インデックスによって [FlipX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowXFormOut** <br/> |
| セル インデックス:  <br/> |**visXFormFlipX** <br/> |
   

