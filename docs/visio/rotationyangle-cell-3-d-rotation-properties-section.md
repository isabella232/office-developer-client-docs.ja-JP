---
title: '[RotationYAngle] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 642d5931-aba3-443d-8c11-d12aa8e56d05
description: Y 軸に沿った回転角度を、° (0.0 ~ 359.9) で指定します。
ms.openlocfilehash: a0ec330ded88aace6c8e4ab658fceca79eb94570
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315590"
---
# <a name="rotationyangle-cell-3-d-rotation-properties-section"></a>[RotationYAngle] セル ([3-D 回転のプロパティ] セクション)

Y 軸に沿った回転角度を、° (0.0 ~ 359.9) で指定します。
  
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[rotationyangle]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[rotationyangle]  <br/> |
   
プログラムから、インデックスによって [ **[rotationyangle]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRow3DRotationProperties** <br/> |
|セル インデックス:  <br/> |**visRotationYAngle** <br/> |
   

