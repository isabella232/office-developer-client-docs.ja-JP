---
title: '[SketchSeed] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: 正の整数として、スケッチ効果のジオメトリを決定するためのランダム化の値を表します。 スケッチ効果が図形に適用すると、SketchSeed のセルの値がランダムに作成されます。
ms.openlocfilehash: 7c9d23e19da1a94bb37f1fc916e2f08095976d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806508"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a>[SketchSeed] セル ([追加効果のプロパティ] セクション)

正の整数として、スケッチ効果のジオメトリを決定するためのランダム化の値を表します。 スケッチ効果が図形に適用すると、 **SketchSeed**のセルの値がランダムに作成されます。 
  
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **SketchSeed** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SketchSeed  <br/> |
   
プログラムから、インデックスによって [ **SketchSeed** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSketchSeed** <br/> |
   

