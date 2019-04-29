---
title: '[RelQuadBezTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: 図形の幅と高さに相対する2次ベジエ曲線の x 座標と y 座標、および図形の幅と高さに相対する曲線のコントロールポイントの x 座標と y 座標を格納します。
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423357"
---
# <a name="relquadbezto-row-geometry-section"></a>[RelQuadBezTo] 行 ([図形座標] セクション)

図形の幅と高さに相対する2次ベジエ曲線の*x*座標と*y*座標、および図形の幅と高さに相対する曲線のコントロールポイントの*x*座標と*y*座標を格納します。 
  
> [!NOTE]
> [**RelQuadBezTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。 Visio 2003-2010 形式でファイルを保存すると、 **[relquadbezto]** 行は[[nurbsto]](nurbsto-row-geometry-section.md)の行に変換されます。 
  
[**RelQuadBezTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |図形の幅を基準にして、2次ベジエ曲線の最後の頂点に対する*x*座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |図形の高さを基準にした、2次ベジエ曲線の最後の頂点に対する*y*座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |図形の幅を基準にして、曲線のコントロールポイントの*x*座標を指定します。弧の点を指定します。コントロールポイントは、円弧の始点と終点の間の中間点を中心に配置されます。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |図形の高さを基準にして、曲線のコントロールポイントの*y*座標です。  <br/> |
   

