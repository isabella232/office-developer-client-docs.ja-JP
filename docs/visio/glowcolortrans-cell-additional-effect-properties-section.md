---
title: '[GlowColorTrans] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6cf67cb-f9e6-43a5-918a-f9151821ab4d
description: 図形の光彩のストロークに使用する色の透過性レベルをパーセンテージで指定します。
ms.openlocfilehash: 81b734de6212540e0f50df05aca11dc535fc49ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326090"
---
# <a name="glowcolortrans-cell-additional-effect-properties-section"></a>[GlowColorTrans] セル ([追加効果のプロパティ] セクション)

図形の光彩のストロークに使用する色の透過性レベルをパーセンテージで指定します。 
  
## <a name="remarks"></a>解説

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**GlowColorTrans**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [glowcolortrans]  <br/> |
   
プログラムから、インデックスによって [**GlowColorTrans**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visGlowColorTrans** <br/> |
   

