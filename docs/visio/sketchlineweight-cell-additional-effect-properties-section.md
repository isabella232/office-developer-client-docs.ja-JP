---
title: '[SketchLineWeight] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: スケッチ効果の結果として、線の太さに追加された厚みを、0 から 50 のポイントで決定します。 [sketchlineweight] セルの値が大きくなるにつれて、図形の線の太さが上がります。
ms.openlocfilehash: 0ee71bbaec59f5c79b72314b08478f8028b4e0ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404513"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a>[SketchLineWeight] セル ([追加効果のプロパティ] セクション)

スケッチ効果の結果として、線の太さに追加された厚みを、0 から 50 のポイントで決定します。 **[sketchlineweight]** セルの値が大きくなるにつれて、図形の線の太さが上がります。 
  
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchLineWeight**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [sketchlineweight]  <br/> |
   
プログラムから、インデックスによって [**SketchLineWeight**] セルへの参照を取得するには、**SketchLineWeight**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSketchLineWeight** <br/> |
   

