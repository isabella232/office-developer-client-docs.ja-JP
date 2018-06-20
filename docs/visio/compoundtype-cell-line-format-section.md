---
title: '[CompoundType] セル ([線の形式] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: 複合図形の線の種類を決定します。
ms.openlocfilehash: 663b683030251c8b57324f1d2bdf492463c50eef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805054"
---
# <a name="compoundtype-cell-line-format-section"></a>[CompoundType] セル ([線の形式] セクション)

複合図形の線の種類を決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |Simple/標準  <br/> |
|1  <br/> |倍精度浮動小数点型 (Double)  <br/> |
|2  <br/> |太さシンします。  <br/> |
|3  <br/> |細い太い  <br/> |
|4  <br/> |トリプル  <br/> |
   
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **CompoundType** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | CompoundType  <br/> |
   
プログラムから、インデックスによって [ **CompoundType** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLine** <br/> |
| セル インデックス:  <br/> |**visCompoundType** <br/> |
   

