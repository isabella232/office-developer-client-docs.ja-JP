---
title: '[SketchSeed] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: スケッチ効果の図形座標を決定するために使用されるランダム化の値を、正の整数で表します。[SketchSeed] セルの値は、スケッチ効果を図形に適用するとき、ランダムで作成されます。
ms.openlocfilehash: 9b7edab031427e34dbff0aac02a4f72110a0821f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549589"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a>[SketchSeed] セル ([追加効果のプロパティ] セクション)

スケッチ効果の図形座標を決定するために使用されるランダム化の値を、正の整数で表します。[**SketchSeed**] セルの値は、スケッチ効果を図形に適用するとき、ランダムで作成されます。 
  
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchSeed**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SketchSeed  <br/> |
   
プログラムから、インデックスによって [**SketchSeed**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSketchSeed** <br/> |
   

