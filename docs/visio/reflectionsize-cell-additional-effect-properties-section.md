---
title: '[ReflectionSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dfeb78e-a0fa-4492-b35f-70b1e2975d38
description: 0.0 から 100.0% の割合として、図形を基準にして反射のサイズを決定します。 ReflectionSize のセルに 0% の値を持つ図形には、リフレクションはありません。100% の値は、図形の完全なミラー イメージを表示します。
ms.openlocfilehash: b525a5f7379b2702dd7152d4eccf6dab1879a6cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806165"
---
# <a name="reflectionsize-cell-additional-effect-properties-section"></a>[ReflectionSize] セル ([追加効果のプロパティ] セクション)

0.0 から 100.0% の割合として、図形を基準にして反射のサイズを決定します。 **ReflectionSize**のセルに 0% の値を持つ図形には、リフレクションはありません。100% の値は、図形の完全なミラー イメージを表示します。 
  
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReflectionSize** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ReflectionSize  <br/> |
   
プログラムから、インデックスによって [ **ReflectionSize** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visReflectionSize** <br/> |
   

