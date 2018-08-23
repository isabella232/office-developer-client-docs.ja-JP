---
title: '[ArcTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: X と y の座標、円弧の弓。
ms.openlocfilehash: 77ed0dcaee7ddefa8771d3e890776d4adfcc3b40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804782"
---
# <a name="arcto-row-geometry-section"></a>[ArcTo] 行 ([図形座標] セクション)

*X*と*y*の座標、円弧の弓。 
  
[ArcTo] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X*の円弧の終点の座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y*の円弧の終点の座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |円弧の中点から弦の中点までの距離です。  <br/> |
   
## <a name="remarks"></a>備考

Visio で描画する弧は、真円に基づいている場合でも、楕円の弧になります。既定では、描画された弧は [シェイプシート] ウィンドウの [EllipticalArcTo] 行で表されます。[ArcTo] 行を [シェイプシート] ウィンドウに表示するには、弧を描画してから、行の種類を [EllipticalArcTo] から [ArcTo] に変更します。この結果、楕円の弧が真円の弧に変換されます。
  
行の種類を変更するには、行を右クリックして、ショートカット メニューの [**図形要素の変更**] をクリックします。 
  

