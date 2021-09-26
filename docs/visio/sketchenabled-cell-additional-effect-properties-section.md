---
title: '[SketchEnabled] セルl ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0baef353-41a1-4071-b5b4-ae342086fe34
description: ブール型 (Boolean) として、図形にスケッチ効果を表示するかどうかを指定します。
ms.openlocfilehash: 552870931687fe5da349fec82c564beed460bb55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603495"
---
# <a name="sketchenabled-cell-additional-effect-properties-section"></a>[SketchEnabled] セルl ([追加効果のプロパティ] セクション)

ブール型 (Boolean) として、図形にスケッチ効果を表示するかどうかを指定します。 
  
## <a name="remarks"></a>注釈

別の数式、Cell 要素の **N** 属性の値、**または CellsU** プロパティを使用したプログラムから、名前によって **[SketchEnabled]** セルへの参照を取得するには、次の値を使用します。  
  
|||
|:-----|:-----|
| セル名:  <br/> | SketchEnabled  <br/> |
   
プログラムから Index によって **[SketchEnabled]** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSketchEnabled** <br/> |
   

