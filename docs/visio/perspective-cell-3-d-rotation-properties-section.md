---
title: '[Perspective] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e07d97a4-9896-4b88-9e76-5a1b3f133094
description: 遠近角度の角度を度 (0 ~ 359.9) で指定します。
ms.openlocfilehash: 4cbefc2fa147a418fa792542e1dc57c39ab2490c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422531"
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
   

