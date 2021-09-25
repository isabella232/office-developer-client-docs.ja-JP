---
title: '[SketchFillChange] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: スケッチ効果を使用する場合の図形の図形の塗りつぶしのランダム化の量を、セクションの長さに対する割合で指定します。 [SketchFillChange] セルの値が 0% に設定されている場合、図形の塗りつぶしの境界ジオメトリは図形のジオメトリと一致します。 値が 100% の場合、図形の塗りつぶしの境界ジオメトリは図形のジオメトリに従います。
ms.openlocfilehash: 8f3b566743c650f930a3c0163e89bfe32b77cabb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598032"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>[SketchFillChange] セル ([追加効果のプロパティ] セクション)

スケッチ効果を使用する場合の図形の図形の塗りつぶしのランダム化の量を、セクションの長さに対する割合で指定します。 **[SketchFillChange] セルの値** が 0% に設定されている場合、図形の塗りつぶしの境界ジオメトリは図形のジオメトリと一致します。 値が 100% の場合、図形の塗りつぶしの境界ジオメトリは図形のジオメトリに従います。 
  
## <a name="remarks"></a>注釈

最適な結果を得るための [**SketchFillChange**] セルの値の理想的な範囲は、15% から 50% の間です。15% を下回る値ではほとんどわからず、50% を上回る値ではランダム化がいっそう強くなります。 
  
別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchFillChange**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SketchFillChange  <br/> |
   
プログラムから、インデックスによって [**SketchFillChange**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSketchFillChange** <br/> |
   

