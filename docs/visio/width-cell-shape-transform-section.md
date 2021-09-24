---
title: '[Width] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
ms.localizationpriority: medium
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 選択した図形の幅を図面の単位で表した値が表示されます。1-D 図形の幅を決定する既定の数式は次のとおりです。
ms.openlocfilehash: 15149ba184176b0a96d26d85296d8c613512e3e9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549323"
---
# <a name="width-cell-shape-transform-section"></a>[Width] セル ([Shape Transform] セクション)

選択した図形の幅を図面の単位で表した値が表示されます。1-D 図形の幅を決定する既定の数式は次のとおりです。
  
= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Width] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Width  <br/> |
   
プログラムから、インデックスによって [Width] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowXFormOut** <br/> |
| セル インデックス:  <br/> |**visXFormWidth** <br/> |
   

