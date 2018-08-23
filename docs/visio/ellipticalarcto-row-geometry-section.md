---
title: '[EllipticalArcTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: 含まれています x および y-楕円の円弧の端点、x および y の座標-、円弧のコントロール ポイントの座標が x の角度の軸には、楕円の長軸、および楕円の長軸と短軸の軸との間の比率。
ms.openlocfilehash: 9a356429f14a20b72a8bd55689855e2954d4a807
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805302"
---
# <a name="ellipticalarcto-row-geometry-section"></a>[EllipticalArcTo] 行 ([図形座標] セクション)

*X*および*y* 、 *x*の楕円の円弧の終点の座標が含まれていますと*y*の、円弧のコントロール ポイントの座標が*x*の角度の軸には、楕円の長軸、および楕円のメジャーと mino の比率。r 軸です。 
  
[EllipticalArcTo] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X*の円弧の終点の座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y*の円弧の終点の座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X*の円弧のコントロール ポイントの座標円弧上の点。コントロール ポイントは、最初と最後の円弧の頂点の間で途中で最適に配置します。それ以外の場合、円弧は、予期しない結果で、コントロール ポイントを通過するために極端になることがあります。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*Y*の円弧のコントロール ポイントの座標です。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |*X*を基準にして、円弧の長軸の角度を親の軸です。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。  <br/> |
   

