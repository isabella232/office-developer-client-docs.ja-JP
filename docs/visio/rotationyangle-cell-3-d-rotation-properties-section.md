---
title: '[RotationYAngle] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 642d5931-aba3-443d-8c11-d12aa8e56d05
description: 度単位で、y 軸方向の回転の角度を設定 (0.0 から 359.9)。
ms.openlocfilehash: 4691b856f35e74a700030a54685831d6e4acdff4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806257"
---
# <a name="rotationyangle-cell-3-d-rotation-properties-section"></a>[RotationYAngle] セル ([3-D 回転のプロパティ] セクション)

度単位で、y 軸方向の回転の角度を設定 (0.0 から 359.9)。
  
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **RotationYAngle** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |RotationYAngle  <br/> |
   
プログラムから、インデックスによって [ **RotationYAngle** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRow3DRotationProperties** <br/> |
|セル インデックス:  <br/> |**visRotationYAngle** <br/> |
   
