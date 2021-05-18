---
title: '[ReflectionSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dfeb78e-a0fa-4492-b35f-70b1e2975d38
description: 図形と相対する反射のサイズを、0.0 から 100.0% までのパーセンテージとして決定します。[ReflectionSize] セルに 0% の値を設定した図形には反射がありません。100% の値を設定すると、図形の完全な鏡像が表示されます。
ms.openlocfilehash: 60fcb315ec1b6187082bdcdbbdcfaa4b80bbcfb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409077"
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
   

