---
title: '[E] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: NURBS (nonuniform rational B-spline) の数式が格納されます。
ms.openlocfilehash: 000c4864c6ae98bfcd9e9cfdb16ff68396f63e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805295"
---
# <a name="e-cell-geometry-section"></a>[E] セル ([図形座標] セクション)

NURBS (nonuniform rational B-spline) の数式が格納されます。
  
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [E] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリの*i*です。E *j* 、 *i*および*j* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [E] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| 行インデックス:  <br/> |**visRowVertex** +  *j* 、 *j* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visNURBSData** <br/> |
   

