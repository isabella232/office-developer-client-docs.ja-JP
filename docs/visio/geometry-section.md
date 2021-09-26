---
title: '[Geometry] セクション'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
ms.localizationpriority: medium
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: 図形を構成する直線と円弧の頂点の座標を一覧表示する行を格納します。
ms.openlocfilehash: 38418376f6296fb3b6f1bbb4e9722421dfcf2440
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598578"
---
# <a name="geometry-section"></a>[Geometry] セクション

図形を構成する直線と円弧の頂点の座標を一覧表示する行を格納します。 
  
図形のジオメトリは、複数の Geometry セクション **で** 表現できます。 複数のパスが異なるプロパティ (イメージ クリッピング パスなど) を持つ場合は、複数 [のパスを使用すると](clippingpath-cell-foreign-image-info-section.md) 便利です。 
  
## <a name="remarks"></a>注釈

**[Geometry]** セクションには、次の行の種類が含まれます。 詳細については、各行のトピックを参照してください。 
  
|行|説明|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |目的の座標に移動します。  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |座標までの線を描画します。  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |座標までの真円の弧を描画します。  <br/> |
|[楕円ArcTo](ellipticalarcto-row-geometry-section.md) <br/> |座標までの楕円の弧を描画します。  <br/> |
|[ポリラインTo](polylineto-row-geometry-section.md) <br/> |座標までのポリラインまたは連続した線を描画します。  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |非一様な合理的な B スプライン (NURBS) を座標に描画します。  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |スプラインを開始します。  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |ノット座標までのスプライン セグメントを描画します。  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |1 つの座標から別の座標に無限線を描画します。  <br/> |
|[楕円](ellipse-row-geometry-section.md) <br/> |中心座標および長軸/短軸から楕円を描画します。  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |図形の幅と高さを基準に 3 次ベジエ曲線を描画します。  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |図形の高さと幅を基準に楕円円弧を座標に描画します。  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |図形の高さと幅を基準に座標に線を描画します。  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |図形の幅と高さを基準に座標に移動します。  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |図形の幅と高さを基準に 2 次ベジエ曲線を描画します。  <br/> |
   
このセクションにある行の種類を変更するには、行を右クリックして、ショートカット メニューの [**図形要素の変更**] をクリックします。 
  

