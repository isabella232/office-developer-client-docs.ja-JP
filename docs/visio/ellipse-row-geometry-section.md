---
title: '[Ellipse] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: 楕円の中心点と楕円上の2つの点に対する x 座標と y 座標を格納します。
ms.openlocfilehash: 5121ba0c7bf97eaeaaf8a438dd40eccddada4362
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345683"
---
# <a name="ellipse-row-geometry-section"></a>[Ellipse] 行 ([Geometry] セクション)

楕円の中心点と楕円上の2つの点に対する*x*座標と*y*座標を格納します。 
  
[Ellipse] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |中心点の*x*座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |中心点の*y*座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |楕円上の1点の x 座標です。対応する*y*座標は [B セルで表されます。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |楕円上の1点の*y*座標です。対応する x 座標は、A セルで表されます。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |楕円上の別の点の*x*座標です。対応する*y*座標は [D セルで表されます。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |楕円上の別の点の*y*座標です。対応する*y*座標は [C セルで表されます。  <br/> |
   
## <a name="remarks"></a>解説

[Ellipse] 行または [InfiniteLine] 行を含む [Geometry] セクションには、他の行を入れることができません。
  

