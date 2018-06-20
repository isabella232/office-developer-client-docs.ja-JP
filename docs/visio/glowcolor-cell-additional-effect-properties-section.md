---
title: '[GlowColor] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 640d18c0-5b6a-4a2f-9c81-f74de5ba9eb1
description: 図形に適用する外側のグローのストロークに使用する色を、RGB またはテーマの値で決定します。
ms.openlocfilehash: 167b08815f345903aed7ff1e92dd750461839dcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805468"
---
# <a name="glowcolor-cell-additional-effect-properties-section"></a>[GlowColor] セル ([追加効果のプロパティ] セクション)

図形に適用する外側のグローのストロークに使用する色を、RGB またはテーマの値で決定します。
  
## <a name="remarks"></a>Remarks

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **GlowColor** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | GlowColor  <br/> |
   
プログラムから、インデックスによって [ **GlowColor** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visGlowColor** <br/> |
   

