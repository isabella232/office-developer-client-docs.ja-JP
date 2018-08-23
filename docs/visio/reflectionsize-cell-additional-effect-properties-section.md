---
title: '[ReflectionSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dfeb78e-a0fa-4492-b35f-70b1e2975d38
description: 図形と相対する反射のサイズを、0.0 から 100.0% までのパーセンテージとして決定します。[ReflectionSize] セルに 0% の値を設定した図形には反射がありません。100% の値を設定すると、図形の完全な鏡像が表示されます。
ms.openlocfilehash: b525a5f7379b2702dd7152d4eccf6dab1879a6cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806165"
---
# <a name="reflectionsize-cell-additional-effect-properties-section"></a>[ReflectionSize] セル ([追加効果のプロパティ] セクション)

図形と相対する反射のサイズを、0.0 から 100.0% までのパーセンテージとして決定します。[**ReflectionSize**] セルに 0% の値を設定した図形には反射がありません。100% の値を設定すると、図形の完全な鏡像が表示されます。 
  
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**ReflectionSize**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ReflectionSize  <br/> |
   
プログラムから、インデックスによって [**ReflectionSize**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visReflectionSize** <br/> |
   

