---
title: '[GlowColor] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 640d18c0-5b6a-4a2f-9c81-f74de5ba9eb1
description: 図形に適用する外側のグローのストロークに使用する色を、RGB またはテーマの値で決定します。
ms.openlocfilehash: babd9a67b1fb6d62c3fbaa2986a6303327cafd53
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574175"
---
# <a name="glowcolor-cell-additional-effect-properties-section"></a>[GlowColor] セル ([追加効果のプロパティ] セクション)

図形に適用する外側のグローのストロークに使用する色を、RGB またはテーマの値で決定します。
  
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**GlowColor**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | GlowColor  <br/> |
   
プログラムから、インデックスによって [**GlowColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visGlowColor** <br/> |
   

