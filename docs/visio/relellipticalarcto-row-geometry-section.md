---
title: '[RelEllipticalArcTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: 含まれています x と y の図形の幅と高さ、x を基準にして楕円の円弧の端点の座標および y-図形の幅と高さを基準にして円弧のコントロール ポイントの座標が x の角度、楕円の長軸、および t の比率を軸彼は楕円の長軸と短軸の軸。
ms.openlocfilehash: 417a2a92bc5c94f9620c7c6f1081ba81d93aa890
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806185"
---
# <a name="relellipticalarcto-row-geometry-section"></a>[RelEllipticalArcTo] 行 ([図形座標] セクション)

*X*と*y* - 図形の幅と高さ、 *x*を基準にして楕円の円弧の端点の座標と*y*が含まれていますが、図形の幅と高さを基準にして円弧のコントロール ポイントの座標が*x*の角度  軸には、楕円の長軸、および楕円の長軸と短軸の軸との比率です。 
  
> [!NOTE]
> **RelEllipticalArcTo**行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保持できます。 Visio 2003 から 2010 年の形式にファイルを保存すると、 **RelEllipticalArcTo**行が[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)の行に変換されます。 
  
[**RelEllipticalArcTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -図形の幅を基準にして円弧の終点の座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -図形の高さを基準にして円弧の終点の座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X* -図形の幅を基準にして、円弧のコントロール ポイントの座標円弧上の点。コントロール ポイントは、最初と最後の円弧の頂点の間で途中で最適に配置します。それ以外の場合、円弧は、予期しない結果で、コントロール ポイントを通過するために極端になることがあります。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*Y* -図形の幅を基準にして、円弧のコントロール ポイントの座標です。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |*X*を基準にして、円弧の長軸の角度を親の軸です。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。  <br/> |
   
## <a name="remarks"></a>Remarks

**RelEllipticalArcTo**行の値は、 [EllipticalArcTo](ellipticalarcto-row-geometry-section.md)行、図形の高さと幅を掛けた値に相当します。 たとえば: **RelEllipticalArcTo**行の**X**、 **Y**、 **A**、 **B** **C**および**D**のセルが値を持つ、1、1、1.5、0.5 15 度、および 1.5 (それぞれ) と交換できます**EllipticalArcTo**行セルの数式`Width*1`、 `Height*1'`、 `Width*1.5`、 `Height*0.5`、15 度、および 1.5 (それぞれ)。
  

