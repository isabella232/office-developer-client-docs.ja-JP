---
title: '[ReflectionBlur] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece15159-6a33-4abd-8775-6fbe1cc43793
description: 図形の反射のぼかしの量を 0.0 ~ 100.0 のポイント単位で指定します。
ms.openlocfilehash: 67ed06d764b90afbc47895c4c714fefadbe6f062
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348399"
---
# <a name="reflectionblur-cell-additional-effect-properties-section"></a>[ReflectionBlur] セル ([追加効果のプロパティ] セクション)

図形の反射のぼかしの量を 0.0 ~ 100.0 のポイント単位で指定します。
  
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[reflectionblur]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [reflectionblur]  <br/> |
   
プログラムから、インデックスによって [ **[reflectionblur]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visReflectionBlur** <br/> |
   

