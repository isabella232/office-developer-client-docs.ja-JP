---
title: '[TxtAngle] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251272
ms.localizationpriority: medium
ms.assetid: b8482cd8-5205-40ef-b4e1-4ceb197ac80f
description: 図形の x 軸に対するテキスト ブロックの現在の回転角度を決定します。 既定値は 0°です。
ms.openlocfilehash: 253c8358e4c1a81d62687030e7ea117f94205402
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569846"
---
# <a name="txtangle-cell-text-transform-section"></a>[TxtAngle] セル ([Text Transform] セクション)

図形の x 軸に対するテキスト ブロックの現在の回転角度を決定します。 既定値は 0°です。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtAngle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | TxtAngle  <br/> |
   
プログラムから、インデックスによって [TxtAngle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormAngle** <br/> |
   

