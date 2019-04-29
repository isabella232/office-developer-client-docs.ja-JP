---
title: '[RotationZAngle] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c39b7f7-1cd7-4e0d-946c-356705194583
description: Z 軸に沿った回転角度を、° (0.0 ~ 359.9) で指定します。
ms.openlocfilehash: 8cabf6995b523cdbd91e7ac54085ad02a2521191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439696"
---
# <a name="rotationzangle-cell-3-d-rotation-properties-section"></a>[RotationZAngle] セル ([3-D 回転のプロパティ] セクション)

Z 軸に沿った回転角度を、° (0.0 ~ 359.9) で指定します。
  
## <a name="remarks"></a>注釈

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[rotationzangle]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[rotationzangle]  <br/> |
   
プログラムから、インデックスによって [ **[rotationzangle]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRow3DRotationProperties** <br/> |
|セル インデックス:  <br/> |**visRotationZAngle** <br/> |
   

