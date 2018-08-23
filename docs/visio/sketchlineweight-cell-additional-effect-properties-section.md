---
title: '[SketchLineWeight] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: 0 から 50 までのポイントで、スケッチ効果の結果として、線の太さに追加されたその他の太さを決定します。 セルが増加する SketchLineWeight の値として図形の線の太さが大きくなります。
ms.openlocfilehash: 9ab99faab907ddf0d944abbeea39672906b4c03d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806522"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a>[SketchLineWeight] セル ([追加効果のプロパティ] セクション)

0 から 50 までのポイントで、スケッチ効果の結果として、線の太さに追加されたその他の太さを決定します。 **SketchLineWeight**のセルが値として図形の線の太さが大きくなります。 
  
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchLineWeight**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SketchLineWeight  <br/> |
   
プログラムから、インデックスによって [**SketchLineWeight**] セルへの参照を取得するには、**SketchLineWeight**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSketchLineWeight** <br/> |
   

