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
description: X および y が含まれています、図形の最初の頂点の座標または x を表すと y のパス内の改行の後の最初の頂点の座標です。
ms.openlocfilehash: cee62701074269350ae52c6fa7f7aee5cb612f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805909"
---
# <a name="moveto-row-geometry-section"></a>[MoveTo] 行 ([図形座標] セクション)

*X*および*y*が含まれています、図形の最初の頂点の座標または*x*を表すと*y*のパス内の改行の後の最初の頂点の座標です。 
  
[**MoveTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |**[Moveto]** 行がセクションの最初の行の場合は、[X] セルは*x*を表しますが、図形の最初の頂点の座標です。 [X] セルが*x*を表す 2 つの行の間、 **[moveto]** 行が表示されている場合のパスを切断した後の最初の頂点の座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |**[Moveto]** 行がセクションの最初の行の場合は、[Y] セルは*y*を表す-図形の最初の頂点の座標です。 [Y] セルが*y*を表す 2 つの行の間、 **[moveto]** 行が表示されている場合のパスを切断した後の最初の頂点の座標です。  <br/> |
   
## <a name="remarks"></a>注釈

**[Moveto]** 行には、 *x*および*y*が含まれています- **[moveto]** 行がセクションの最初の行である場合の図形の最初の頂点の座標です。 通常これは図形が描画されて、および 1-d 図形の始点に必ずしも対応していないときに配置する最初の頂点です。 
  
[Geometry] セクションは、 **RelMoveTo**または **[moveto]** 行では、いずれかで始まる必要がありますが、図形のパスの描画にギャップを表すため、 **[moveto]** 行と**RelMoveTo**行を使用することもできます。 ただし、塗りつぶされた領域の境界を定義するのには、パスを使用する場合は、このギャップが直線セグメントとして解釈されます。 このようなギャップを挿入するには、2 つの行の間で行を挿入し、行の種類を **[moveto]** に変更します。 **[Moveto]** 行が 2 行の間にある場合は、含まれている、 *x*および*y*の図形のパスを切断した後の行の最初の頂点の座標です。 
  

