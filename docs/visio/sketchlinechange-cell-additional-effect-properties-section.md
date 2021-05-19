---
title: '[SketchLineChange] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: スケッチ効果を使用する場合の図形のジオメトリからの図形の線のランダム化の量を、セクションの長さに対するパーセンテージで指定します。 [SketchLineChange] セルの値が 0% に設定されている場合、図形の線のジオメトリは図形のジオメトリと一致します。 値が 100% の場合、図形の線のジオメトリは図形のジオメトリに従います。
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419507"
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
   

