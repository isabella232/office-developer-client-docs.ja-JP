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
description: 円弧の x 座標と y 座標、および弧を格納します。
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341406"
---
# <a name="arcto-row-geometry-section"></a>[ArcTo] 行 ([Geometry] セクション)

円弧の*x*座標と*y*座標、および弧を格納します。 
  
[ArcTo] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |円弧の最後の頂点に対する*x*座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |円弧の最後の頂点に対する*y*座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |円弧の中点から弦の中点までの距離です。  <br/> |
   
## <a name="remarks"></a>解説

Visio で描画する弧は、真円に基づいている場合でも、楕円の弧になります。既定では、描画された弧は [シェイプシート] ウィンドウの [EllipticalArcTo] 行で表されます。[ArcTo] 行を [シェイプシート] ウィンドウに表示するには、弧を描画してから、行の種類を [EllipticalArcTo] から [ArcTo] に変更します。この結果、楕円の弧が真円の弧に変換されます。
  
行の種類を変更するには、行を右クリックして、ショートカット メニューの [**図形要素の変更**] をクリックします。 
  

