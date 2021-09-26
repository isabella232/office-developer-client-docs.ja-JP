---
title: '[KeepTextFlat] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: 図形のテキストが 3-D での図形の回転を無視するかどうかを示します。 2-D 回転には適用されません。
ms.openlocfilehash: a37cfabe00742f7850fd1fa9a1faab7a6be8e5a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618743"
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
   

