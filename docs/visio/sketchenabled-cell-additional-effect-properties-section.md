---
title: '[SketchEnabled] セルl ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0baef353-41a1-4071-b5b4-ae342086fe34
description: 図形の上またはブール値としてではなく、スケッチ効果が表示されるかどうかを決定します。
ms.openlocfilehash: 7428d54eccce1a62d95a78dbc5fc6770fa5f1a77
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806506"
---
# <a name="sketchenabled-cell-additional-effect-properties-section"></a>[SketchEnabled] セルl ([追加効果のプロパティ] セクション)

図形の上またはブール値としてではなく、スケッチ効果が表示されるかどうかを決定します。 
  
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **SketchEnabled** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SketchEnabled  <br/> |
   
プログラムから、インデックスによって [ **SketchEnabled** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSketchEnabled** <br/> |
   

