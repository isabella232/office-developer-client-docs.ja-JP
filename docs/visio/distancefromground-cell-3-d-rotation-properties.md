---
title: '[DistanceFromGround] セル ([3-D 回転のプロパティ)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87499dab-977a-45bc-9f6a-8daa80a82abb
description: 3-D で回転した場合に、オブジェクトが地面からポイントで上がる距離を決定します。
ms.openlocfilehash: aa2f1629ecad234d85d4393411bd40215a671e1d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405619"
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
   

