---
title: '[ReflectionBlur] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece15159-6a33-4abd-8775-6fbe1cc43793
description: 図形の反射のぼかしの量を 0.0 ~ 100.0 のポイントで指定します。
ms.openlocfilehash: 67ed06d764b90afbc47895c4c714fefadbe6f062
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408013"
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
   

