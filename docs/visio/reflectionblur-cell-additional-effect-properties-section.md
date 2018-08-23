---
title: '[ReflectionBlur] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece15159-6a33-4abd-8775-6fbe1cc43793
description: 0.0 から 100.0 までのポイント単位で、図形上の反射のぼかしの量を決定します。
ms.openlocfilehash: d283531cc10b7a18952dcef398acf050c91bafb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806166"
---
# <a name="reflectionblur-cell-additional-effect-properties-section"></a>[ReflectionBlur] セル ([追加効果のプロパティ] セクション)

0.0 から 100.0 までのポイント単位で、図形上の反射のぼかしの量を決定します。
  
## <a name="remarks"></a>注釈

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReflectionBlur** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ReflectionBlur  <br/> |
   
プログラムから、インデックスによって [ **ReflectionBlur** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visReflectionBlur** <br/> |
   

