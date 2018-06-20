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
description: X および y が含まれていますが、楕円の中心点および楕円上の 2 つの点の座標です。
ms.openlocfilehash: 0a2acb0efa20f67d04581f827edbfc4fb4a2d6b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805300"
---
# <a name="ellipse-row-geometry-section"></a>[Ellipse] 行 ([Geometry] セクション)

*X*および*y*が含まれていますが、楕円の中心点および楕円上の 2 つの点の座標です。 
  
[Ellipse] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X*の中心点の座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y*の中心点の座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |楕円上の 1 つの点の x 座標対応する*y*の座標は、[B] セルで表されます。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*Y* -楕円上の 1 つの点の座標対応する x 座標は [A] セルで表されます。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |*X* -楕円上の別の点の座標対応する*y*の座標は [D] セルで表されます。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |*Y* -楕円上の別の点の座標対応する*y*の座標は、[C] セルで表されます。  <br/> |
   
## <a name="remarks"></a>備考

[Ellipse] 行または [InfiniteLine] 行を含む [Geometry] セクションには、他の行を入れることができません。
  

