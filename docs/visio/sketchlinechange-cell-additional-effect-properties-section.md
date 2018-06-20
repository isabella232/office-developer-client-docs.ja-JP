---
title: '[SketchLineChange] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: セクションの長さの割合として、スケッチ効果を使用する場合は、図形の線を図形の座標からのランダム化の量を決定します。 SketchLineChange セルの値を 0% に設定すると、図形の線のジオメトリは、図形の座標を一致します。 値が 100% の場合は、図形の線のジオメトリは、図形のジオメトリを従っていません。
ms.openlocfilehash: 57d2af1a914710d7e5a58686b577014ceb7af424
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806505"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>[SketchLineChange] セル ([追加効果のプロパティ] セクション)

セクションの長さの割合として、スケッチ効果を使用する場合は、図形の線を図形の座標からのランダム化の量を決定します。 **SketchLineChange**セルの値を 0% に設定すると、図形の線のジオメトリは、図形の座標を一致します。 値が 100% の場合は、図形の線のジオメトリは、図形のジオメトリを従っていません。 
  
## <a name="remarks"></a>備考

最良の結果を得るには、理想的な**SketchLineChange**のセルの値の範囲は 15% と 50% の間では。 15% 未満の値はほとんど気になりません。50% より大きい値は、行をあまりランダムでした。 
  
**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **SketchLineChange** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SketchLineChange  <br/> |
   
プログラムから、インデックスによって [ **SketchLineChange** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSketchLineChange** <br/> |
   

