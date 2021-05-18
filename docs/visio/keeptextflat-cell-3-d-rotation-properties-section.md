---
title: '[KeepTextFlat] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: 図形のテキストが 3-D での図形の回転を無視するかどうかを示します。 2-D 回転には適用されません。
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422041"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>[KeepTextFlat] セル ([3-D 回転のプロパティ] セクション)

図形のテキストが 3-D での図形の回転を無視するかどうかを示します。 2-D 回転には適用されません。 
  
****

|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形テキストは、図形のジオメトリと一緒に回転されません。  <br/> |
|FALSE  <br/> |図形のテキストは、図形のジオメトリと一緒に回転するために変換されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**KeepTextFlat**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |KeepTextFlat  <br/> |
   
プログラムから、インデックスによって [**KeepTextFlat**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRow3DRotationProperties** <br/> |
|セル インデックス:  <br/> |**visKeepTextFlat** <br/> |
   

