---
title: '[Geometry] セクション'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: 直線と図形を構成する円弧の頂点の座標を一覧表示する行が含まれています。
ms.openlocfilehash: 59f85c512b7038f6cfddcb657435730a2e724bd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805462"
---
# <a name="geometry-section"></a>[Geometry] セクション

直線と図形を構成する円弧の頂点の座標を一覧表示する行が含まれています。 
  
**ジオメトリ**の複数のセクションでは、図形の形状を表すことができます。 複数のパスは、さまざまなプロパティ ([イメージのクリッピング](clippingpath-cell-foreign-image-info-section.md)・ パスなど) を複数のパスがあるときに役に立ちます。 
  
## <a name="remarks"></a>備考

**[Geometry** ] セクションには、次の行の種類が含まれています。 詳細については、各行のトピックを参照してください。 
  
|**Row**|**説明**|
|:-----|:-----|
|[[Moveto]](moveto-row-geometry-section.md) <br/> |目的の座標に移動します。  <br/> |
|[[Lineto]](lineto-row-geometry-section.md) <br/> |座標までの線を描画します。  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |座標までの真円の弧を描画します。  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |座標までの楕円の弧を描画します。  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |座標までのポリラインまたは連続した線を描画します。  <br/> |
|[[Nurbsto]](nurbsto-row-geometry-section.md) <br/> |座標までの一様でない回転 B-スプライン (NURBS) を描画します。  <br/> |
|[[A](splinestart-row-geometry-section.md) <br/> |スプラインを開始します。  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |ノット座標までのスプライン セグメントを描画します。  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |1 つの座標から別の座標に無限線を描画します。  <br/> |
|[楕円](ellipse-row-geometry-section.md) <br/> |中心座標および長軸/短軸から楕円を描画します。  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |図形の高さと幅を基準にして 3 次ベジエ曲線を描画します。  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |図形の幅と高さを基準にして座標を楕円の円弧を描画します。  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |図形の幅と高さは、相対座標に線を引きます。  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |図形の高さと幅を基準にして座標に移動します。  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |図形の高さと幅の 2 次ベジエ曲線を描画します。  <br/> |
   
このセクション内の行タイプを変更するのには、行を右クリックし、し、ショートカット メニューの [**行の種類の変更**] をクリックします。 
  

