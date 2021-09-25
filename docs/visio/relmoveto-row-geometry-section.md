---
title: '[RelMoveTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: 図形の最初の頂点の x 座標と y 座標、またはパス内のブレーク後の最初の頂点の x 座標と y 座標を、図形の高さと幅に対して格納します。
ms.openlocfilehash: 1878a8663ef72fbb5f248a160c0abd0d20458baa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598389"
---
# <a name="relmoveto-row-geometry-section"></a>[RelMoveTo] 行 ([図形座標] セクション)

図形の最初の頂点の  *x*  座標と  *y*  座標、またはパス内のブレーク後の最初の頂点の  *x*  座標と  *y*  座標を、図形の高さと幅に対して格納します。 
  
> [!NOTE]
> [**RelMoveTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。 ファイルを 2003- 2010 Visioに保存すると **、RelMoveTo** 行は [MoveTo 行に変換](moveto-row-geometry-section.md)されます。 
  
[**RelMoveTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |**RelMoveTo** 行がセクションの最初の行である場合、X セルは図形の幅に対する図形の最初の頂点の *x* 座標を表します。 **RelMoveTo** 行が 2 行の間に表示される場合、X セルはパスのブレーク後の最初の頂点の *x* 座標を表します。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |**RelMoveTo** 行がセクションの最初の行である場合、Y セルは図形の最初の頂点の *y* 座標を表します。 **RelMoveTo** 行が 2 行の間に表示される場合、Y セルはパスのブレーク後の最初の頂点の *y* 座標を表します。  <br/> |
   
## <a name="remarks"></a>注釈

[**RelMoveTo**] 行の値は、図形の幅と高さを乗算した [[MoveTo](moveto-row-geometry-section.md)] 行の値に等しくなります。 たとえば **、X** セルの値が "0" で **、Y** セルの値が "0.5" の **RelMoveTo** 行を **MoveTo** 行に置き換え **、X** セルの値が数式 "Width *0" で **、Y*** セルが数式 "Height 0.5" に置き換えられる可能性があります。 
  
**RelMoveTo** 行には、MoveTo 行がセクションの最初の行である場合、図形の最初の頂点の *x* 座標と *y* 座標が含まれる。 通常、これは図形が描画された時点で最初に配置される頂点であり、必ずしも 1-D 図形の開始点に対応するとは限りません。 
  
Geometryセクションは **MoveTo** 行または **RelMoveTo** 行で始まる必要がありますが **、RelMoveTo** 行と **MoveTo** 行を使用して、図形の幅と高さに対する図形のパスのストロークのギャップを表することもできます。 ただし、塗りつぶされた領域の境界を定義するためにパスを使用すると、このギャップは直線セグメントとして解釈されます。 このようなギャップを挿入するには、2 つの行の間に行を挿入し、行の種類を **RelMoveTo に変更します**。 **RelMoveTo** 行が 2 行の間にある場合は、図形のパスのブレーク後の線の最初の頂点の *x* 座標と *y* 座標が含まれます。 
  

