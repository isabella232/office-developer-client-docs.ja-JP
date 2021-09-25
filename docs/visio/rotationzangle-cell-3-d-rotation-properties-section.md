---
title: '[RotationZAngle] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3c39b7f7-1cd7-4e0d-946c-356705194583
description: Z 軸に沿った回転角度を度 (0.0 ~ 359.9) で指定します。
ms.openlocfilehash: e698304c360e7357d8c1bde3c5aebd4da99d0c11
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554083"
---
# <a name="rotationzangle-cell-3-d-rotation-properties-section"></a>[RotationZAngle] セル ([3-D 回転のプロパティ] セクション)

Z 軸に沿った回転角度を度 (0.0 ~ 359.9) で指定します。
  
## <a name="remarks"></a>注釈

別の数式 **、Cell** 要素の **N** 属性の値、または **CellsU** プロパティを使用したプログラムから、名前によって **RotationZAngle** セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |RotationZAngle  <br/> |
   
プログラムから Index によって **RotationZAngle** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRow3DRotationProperties** <br/> |
|セル インデックス:  <br/> |**visRotationZAngle** <br/> |
   

