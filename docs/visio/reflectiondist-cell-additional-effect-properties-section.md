---
title: '[ReflectionDist] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 858a3191-420a-4065-9180-ebd8503d1eef
description: 反射を図形からオフセットする距離を 0.0 ~ 100.0 の範囲で指定します。
ms.openlocfilehash: cc0aca484a77602b78523819cd4f01d78a9ff86f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348385"
---
# <a name="reflectiondist-cell-additional-effect-properties-section"></a>[ReflectionDist] セル ([追加効果のプロパティ] セクション)

反射を図形からオフセットする距離を 0.0 ~ 100.0 の範囲で指定します。 
  
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[reflectiondist]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [reflectiondist]  <br/> |
   
プログラムから、インデックスによって [ **[reflectiondist]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visReflectionDist** <br/> |
   

