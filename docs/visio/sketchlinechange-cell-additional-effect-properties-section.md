---
title: '[SketchLineChange] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: スケッチ効果を使用する場合の図形のジオメトリからの図形の線のランダム化の量を、セクションの長さに対するパーセンテージで指定します。 [SketchLineChange] セルの値が 0% に設定されている場合、図形の線のジオメトリは図形のジオメトリと一致します。 値が 100% の場合、図形の線のジオメトリは図形のジオメトリに従います。
ms.openlocfilehash: 39a5726354ac350e289e6b114f3c1664d2a1aeae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549582"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>[SketchLineChange] セル ([追加効果のプロパティ] セクション)

スケッチ効果を使用する場合の図形のジオメトリからの図形の線のランダム化の量を、セクションの長さに対するパーセンテージで指定します。 **[SketchLineChange]** セルの値が 0% に設定されている場合、図形の線のジオメトリは図形のジオメトリと一致します。 値が 100% の場合、図形の線のジオメトリは図形のジオメトリに従います。 
  
## <a name="remarks"></a>注釈

最適な結果を得るための [**SketchLineChange**] セルの値の理想的な範囲は、15% から 50% の間です。15% を下回る値ではほとんどわからず、50% を上回る値では線が過度にランダム化される可能性があります。 
  
別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchLineChange**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SketchLineChange  <br/> |
   
プログラムから、インデックスによって [**SketchLineChange**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSketchLineChange** <br/> |
   

