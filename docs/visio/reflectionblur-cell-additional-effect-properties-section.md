---
title: '[ReflectionBlur] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ece15159-6a33-4abd-8775-6fbe1cc43793
description: 図形の反射のぼかしの量を 0.0 ~ 100.0 のポイントで指定します。
ms.openlocfilehash: e3c18cf2016f8b213d37061cfb216f8e76bf2e37
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570275"
---
# <a name="reflectionblur-cell-additional-effect-properties-section"></a>[ReflectionBlur] セル ([追加効果のプロパティ] セクション)

図形の反射のぼかしの量を 0.0 ~ 100.0 のポイントで指定します。
  
## <a name="remarks"></a>注釈

別の数式 **、Cell** 要素 **の N** 属性の値、または CellsU プロパティを使用したプログラムから、名前によって **ReflectionBlur** セルへの参照を取得するには、次の値を **使用** します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ReflectionBlur  <br/> |
   
プログラムからインデックスによって **ReflectionBlur** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visReflectionBlur** <br/> |
   

