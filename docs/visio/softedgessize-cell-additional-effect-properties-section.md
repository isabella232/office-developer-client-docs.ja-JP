---
title: '[SoftEdgesSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a5cde2ca-f343-4a6e-b5d9-a1b78b3cd240
description: ソフト エッジ効果のサイズを、0.00 から 100.00 までのポイントで決定します。[SoftEdgesSize] セルの値が 0 の場合、図形にソフト エッジは適用されません。
ms.openlocfilehash: 5d46200feb034b88248c4591136457cd8c99607f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569952"
---
# <a name="softedgessize-cell-additional-effect-properties-section"></a>[SoftEdgesSize] セル ([追加効果のプロパティ] セクション)

ソフト エッジ効果のサイズを、0.00 から 100.00 までのポイントで決定します。[**SoftEdgesSize**] セルの値が 0 の場合、図形にソフト エッジは適用されません。 
  
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SoftEdgesSize**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SoftEdgesSize  <br/> |
   
プログラムから、インデックスによって **SoftEdgesSize**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSoftEdgesSize** <br/> |
   

