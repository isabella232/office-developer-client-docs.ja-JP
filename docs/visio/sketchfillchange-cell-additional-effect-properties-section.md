---
title: '[SketchFillChange] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: スケッチ効果を使用する場合の図形の図形の塗りつぶしのランダム化の量を、セクションの長さに対する割合で指定します。 [SketchFillChange] セルの値が 0% に設定されている場合、図形の塗りつぶしの境界ジオメトリは図形のジオメトリと一致します。 値が 100% の場合、図形の塗りつぶしの境界ジオメトリは図形のジオメトリに従います。
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408076"
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
   

