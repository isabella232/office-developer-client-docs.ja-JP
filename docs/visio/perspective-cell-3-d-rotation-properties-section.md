---
title: '[Perspective] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e07d97a4-9896-4b88-9e76-5a1b3f133094
description: 遠近角度の角度を度 (0 ~ 359.9) で指定します。
ms.openlocfilehash: 2171d8d36ad67ee38df4dfabefde1bccf54b4258
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623230"
---
# <a name="perspective-cell-3-d-rotation-properties-section"></a>[Perspective] セル ([3-D 回転のプロパティ] セクション)

遠近角度の角度を度 (0 ~ 359.9) で指定します。
  
## <a name="remarks"></a>注釈

別の数式、Cell要素 **の N** 属性の値、**または CellsU** プロパティを使用したプログラムから、名前によって [パースペクティブ] セルへの参照を取得するには、次の値を **使用** します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Perspective  <br/> |
   
プログラムからインデックスによって **[パース** ペクティブ] セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRow3DRotationProperties** <br/> |
|セル インデックス:  <br/> |**visPerspective** <br/> |
   

