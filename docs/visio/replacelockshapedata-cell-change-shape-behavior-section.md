---
title: '[ReplaceLockShapeData] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。ReplaceLockShapeData は、マスター シェイプの図形データが、置換される図形の図形データすべてに優先するかどうかを決定します。
ms.openlocfilehash: 98e6c5be4519a55f0207df53dc169604c0718cb4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627647"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>[ReplaceLockShapeData] セル ([図形の動作の変更] セクション)

マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。**ReplaceLockShapeData** は、マスター シェイプの図形データが、置換される図形の図形データすべてに優先するかどうかを決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|1 (TRUE)  <br/> |マスター シェイプの [**Shape Data**] セクションにあるすべての行と値は、置換後の図形にコピーされ、置換される古い図形のローカル値はすべて破棄されます。  <br/> |
|0 (FALSE)  <br/> |マスター シェイプの [**図形データ**] セクションの行と値は、置換される図形にコピーされます。ローカル値を使用した古い図形の [**図形データ**] セクションの行は、置換後の図形に転送されます。<br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**ReplaceLockShapeData**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ReplaceLockShapeData  <br/> |
   
プログラムから、インデックスによって [**ReplaceLockShapeData**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowReplaceBehaviors** <br/> |
| セル インデックス:  <br/> |**visReplaceLockShapeData** <br/> |
   

