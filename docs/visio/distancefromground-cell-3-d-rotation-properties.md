---
title: '[DistanceFromGround] セル ([3-D 回転のプロパティ)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 87499dab-977a-45bc-9f6a-8daa80a82abb
description: 3-D で回転した場合に、オブジェクトが地面からポイントで上がる距離を決定します。
ms.openlocfilehash: 0430f348d55f034206305e15f14d48d7952e6185
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582800"
---
# <a name="distancefromground-cell-3-d-rotation-properties"></a>[DistanceFromGround] セル ([3-D 回転のプロパティ] セクション)

3-D で回転した場合に、オブジェクトが地面からポイントで上がる距離を決定します。
  
## <a name="remarks"></a>注釈

別の数式 **、Cell** 要素の **N** 属性の値、または **CellsU** プロパティを使用したプログラムから、名前によって **DistanceFromGround** セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |DistanceFromGround  <br/> |
   
プログラムからインデックスによって **DistanceFromGround** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRow3DRotationProperties** <br/> |
|セル インデックス:  <br/> |**visDistanceFromGround** <br/> |
   

