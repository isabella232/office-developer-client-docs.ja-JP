---
title: '[RotationType] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: 図形が並行回転、視点回転、または斜め回転に従って回転するかどうかを、0 から 6 までの整数で決定します。
ms.openlocfilehash: 7e5929b4bc80ae499174c3f7c290de4d6e5666ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573503"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>[RotationType] セル ([3-D 回転のプロパティ] セクション)

図形が並行回転、視点回転、または斜め回転に従って回転するかどうかを、0 から 6 までの整数で決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |図形に回転は適用されません。  <br/> |
|1  <br/> |図形に並行回転が適用されます。  <br/> |
|2  <br/> |図形に視点回転が適用されます。  <br/> |
|3  <br/> |図形に左上の斜め回転が適用されます。  <br/> |
|4   <br/> |図形に右上の斜め回転が適用されます。  <br/> |
|5  <br/> |図形に左下の斜め回転が適用されます。  <br/> |
|6   <br/> |図形に右下の斜め回転が適用されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**RotationType**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |RotationType  <br/> |
   
プログラムから、インデックスによって [**RotationType**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRow3DRotationProperties** <br/> |
|セル インデックス:  <br/> |**visRotationType** <br/> |
   

