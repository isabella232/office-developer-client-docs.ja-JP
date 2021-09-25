---
title: '[ArcTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
ms.localizationpriority: medium
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: 円弧の x 座標と y 座標と弓を格納します。
ms.openlocfilehash: 28cf822d71021d7fe4264dd6b4269974e3a75bb6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603915"
---
# <a name="arcto-row-geometry-section"></a>[ArcTo] 行 ([Geometry] セクション)

円弧の  *x*  座標と  *y*  座標と弓を格納します。 
  
[ArcTo] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |円弧  *の*  終了頂点の x 座標。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |円弧  *の終了*  頂点の y 座標。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |円弧の中点から弦の中点までの距離です。  <br/> |
   
## <a name="remarks"></a>注釈

Visio で描画する弧は、真円に基づいている場合でも、楕円の弧になります。既定では、描画された弧は [シェイプシート] ウィンドウの [EllipticalArcTo] 行で表されます。[ArcTo] 行を [シェイプシート] ウィンドウに表示するには、弧を描画してから、行の種類を [EllipticalArcTo] から [ArcTo] に変更します。この結果、楕円の弧が真円の弧に変換されます。
  
行の種類を変更するには、行を右クリックして、ショートカット メニューの [**図形要素の変更**] をクリックします。 
  

