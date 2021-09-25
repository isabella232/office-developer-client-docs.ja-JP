---
title: '[MoveTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
ms.localizationpriority: medium
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: 図形の最初の頂点の x 座標と y 座標、またはパスのブレーク後の最初の頂点の x 座標と y 座標を表します。
ms.openlocfilehash: 77328e6a8b08099d42703034beb32c3835e2cb8c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573881"
---
# <a name="moveto-row-geometry-section"></a>[MoveTo] 行 ([Geometry] セクション)

図形の最初の頂点の  *x*  座標と  *y*  座標、またはパスのブレーク後の最初の頂点の  *x*  座標と  *y*  座標を表します。 
  
[**MoveTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |**MoveTo 行** がセクションの最初の行である場合、X セルは図形の最初の頂点の *x* 座標を表します。 **MoveTo 行が 2** 行の間に表示される場合、X セルはパスのブレーク後の最初の頂点の *x* 座標を表します。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |**MoveTo 行** がセクションの最初の行である場合、Y セルは図形の最初の頂点の *y* 座標を表します。 **MoveTo 行が 2** 行の間に表示される場合、Y セルはパスのブレーク後の最初の頂点の *y* 座標を表します。  <br/> |
   
## <a name="remarks"></a>注釈

**MoveTo 行** には *、MoveTo* 行がセクションの最初の行である場合、図形の最初の頂点の x 座標と *y* 座標が含まれる。 通常、これは図形が描画された時点で最初に配置される頂点であり、必ずしも 1-D 図形の開始点に対応するとは限りません。 
  
ジオメトリ セクションは **RelMoveTo** 行または **MoveTo** 行で始まる必要がありますが **、MoveTo** 行と **RelMoveTo** 行を使用して、図形のパスのストロークのギャップを表することもできます。 ただし、塗りつぶされた領域の境界を定義するためにパスを使用すると、このギャップは直線セグメントとして解釈されます。 このようなギャップを挿入するには、2 つの行の間に行を挿入し、行の種類を **MoveTo に変更します**。 **MoveTo 行が 2** 行の間にある場合、図形のパスでブレークした後の線の最初の頂点の *x* 座標と *y* 座標が含まれます。 
  

