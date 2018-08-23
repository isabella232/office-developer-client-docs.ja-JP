---
title: '[SoftEdgesSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a5cde2ca-f343-4a6e-b5d9-a1b78b3cd240
description: ソフト エッジ効果のサイズを、0.00 から 100.00 までのポイントで決定します。[SoftEdgesSize] セルの値が 0 の場合、図形にソフト エッジは適用されません。
ms.openlocfilehash: 3b301ae2e8c82867be2a486f2e93c2275fbf3914
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806538"
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
   

