---
title: '[MoveTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
localization_priority: Normal
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: 図形の最初の頂点に対する x 座標と y 座標を格納します。または、パスを切断した後の最初の頂点に対する x 座標と y 座標を表します。
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429699"
---
# <a name="moveto-row-geometry-section"></a>[MoveTo] 行 ([Geometry] セクション)

図形の最初の頂点に対する*x*座標と*y*座標を格納します。または、パスを切断した後の最初の頂点に対する*x*座標と*y*座標を表します。 
  
[**MoveTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |[ **MoveTo** ] 行がセクションの最初の行の場合、[x] セルは、図形の最初の頂点に対する*x*座標を表します。 [ **MoveTo** ] 行が2つの行の間に表示される場合、[x] セルは、パスを切断した後の最初の頂点に対する*x*座標を表します。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |[ **MoveTo** ] 行がセクションの最初の行の場合、[y] セルは、図形の最初の頂点に対する*y*座標を表します。 [ **MoveTo** ] 行が2つの行の間に表示される場合、[y] セルは、パスを切断した後の最初の頂点に対する*y*座標を表します。  <br/> |
   
## <a name="remarks"></a>注釈

[ **moveto** ] 行には、[ **moveto** ] 行がセクションの最初の行である場合に、図形の最初の頂点に対する*x*座標と*y*座標が含まれます。 通常、これは図形が描画されたときに最初に配置される頂点で、1-d 図形の始点には必ずしも対応していません。 
  
[geometry] セクションは、[ **relmoveto** ] 行または [ **moveto** ] 行で開始する必要がありますが、図形のパスの描画のギャップを表すのには、 **moveto**と**relmoveto**の行を使用することもできます。 ただし、パスを使用して塗りつぶされた領域の境界を定義すると、このギャップは直線セグメントとして解釈されます。 このような隙間を挿入するには、2つの行の間に行を挿入し、その行の種類を [ **MoveTo**] に変更します。 [ **MoveTo** ] 行が2つの行の間にある場合は、図形のパスにある改行の後の最初の頂点に対する*x*座標と*y*座標を格納します。 
  

