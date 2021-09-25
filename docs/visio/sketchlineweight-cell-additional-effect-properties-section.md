---
title: '[SketchLineWeight] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: スケッチ効果の結果として、線の太さに追加された厚みを、0 から 50 のポイントで決定します。 [SketchLineWeight] セルの値が大きほど、図形の線の太さが増します。
ms.openlocfilehash: 935254e6ed7618279a43fe81eda1cf6835e455f4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553817"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a>[SketchLineWeight] セル ([追加効果のプロパティ] セクション)

スケッチ効果の結果として、線の太さに追加された厚みを、0 から 50 のポイントで決定します。 **[SketchLineWeight]** セルの値が大きほど、図形の線の太さが増します。 
  
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchLineWeight**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SketchLineWeight  <br/> |
   
プログラムから、インデックスによって [**SketchLineWeight**] セルへの参照を取得するには、**SketchLineWeight** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSketchLineWeight** <br/> |
   

