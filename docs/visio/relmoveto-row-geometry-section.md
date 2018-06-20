---
title: '[RelMoveTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: X と y の最初の頂点、図形の x 座標の y が含まれていますが、図形の幅と高さを基準にして、パス内の改行の後の最初の頂点の座標です。
ms.openlocfilehash: 77b3e731bfd1f35abe34ffbf3155b57133e56412
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806198"
---
# <a name="relmoveto-row-geometry-section"></a>[RelMoveTo] 行 ([図形座標] セクション)

*X*と*y*の最初の頂点、図形の*x*座標を*y*が含まれていますが、図形の幅と高さを基準にして、パス内の改行の後の最初の頂点の座標です。 
  
> [!NOTE]
> **RelMoveTo**行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保持できます。 Visio 2003 から 2010 年の形式にファイルを保存すると、 **RelMoveTo**の行は[[moveto]](moveto-row-geometry-section.md)行に変換されます。 
  
**RelMoveTo**行には、次のセルが含まれています。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |**RelMoveTo**行がセクションの最初の行の場合は、[X] セルは*x*を表しますが、図形の幅を基準に図形の最初の頂点の座標。 [X] セルが*x*を表す 2 つの行の間に**RelMoveTo**行が表示されている場合のパスを切断した後の最初の頂点の座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |[Y] セルが*y*を表す**RelMoveTo**の行がセクションの最初の行の場合は、最初の図形の頂点の座標です。 [Y] セルが*y*を表す 2 つの行の間に**RelMoveTo**行が表示されている場合のパスを切断した後の最初の頂点の座標です。  <br/> |
   
## <a name="remarks"></a>備考

**RelMoveTo**行の値は、 [[moveto]](moveto-row-geometry-section.md)行で、幅と図形の高さを乗じた値に相当します。 例: [ **X** ] セルの値が数式にある **[moveto]** 行で [ **X** ] セルの値が「0」は、[ **Y** ] セルの値は「0.5」は、 **RelMoveTo**行を置き換えることができます」*0"の幅] と [ **Y** ] セルは、数式"高さ*0.5」。 
  
**RelMoveTo**行には、 *x*および*y*が含まれています-[moveto] 行がセクションの最初の行である場合の図形の最初の頂点の座標です。 通常これは図形が描画されて、および 1-d 図形の始点に必ずしも対応していないときに配置する最初の頂点です。 
  
**[Geometry** ] セクションを **[moveto]** または**RelMoveTo**の行を開始する必要がありますが、図形の幅と高さを基準にして図形のパスの描画にギャップを表すため、 **RelMoveTo**の行と **[moveto]** 行を使用することもできます。 ただし、塗りつぶされた領域の境界を定義するのには、パスを使用する場合は、このギャップが直線セグメントとして解釈されます。 このようなギャップを挿入するには、2 つの行の間で行を挿入し、行の種類を**RelMoveTo**に変更します。 **RelMoveTo**行が 2 行の間にある場合は、含まれている、 *x*および*y*の図形のパスを切断した後の行の最初の頂点の座標です。 
  

