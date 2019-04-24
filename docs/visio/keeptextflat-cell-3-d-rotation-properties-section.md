---
title: '[KeepTextFlat] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: 図形のテキストが3-d 図形の回転を無視するかどうかを示します。 2-D 回転には適用されません。
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360439"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>[KeepTextFlat] セル ([3-D 回転のプロパティ] セクション)

図形のテキストが3-d 図形の回転を無視するかどうかを示します。 2-D 回転には適用されません。 
  
****

|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形のテキストは、図形の座標を使用して回転しません。  <br/> |
|FALSE  <br/> |図形のテキストは、図形の座標を使用して回転するように変換されます。  <br/> |
   
## <a name="remarks"></a>解説

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**KeepTextFlat**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[keeptextflat]  <br/> |
   
プログラムから、インデックスによって [**KeepTextFlat**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRow3DRotationProperties** <br/> |
|セル インデックス:  <br/> |**visKeepTextFlat** <br/> |
   

