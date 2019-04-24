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
description: 図形を構成する直線と円弧の頂点の座標を一覧表示する行を格納します。
ms.openlocfilehash: 32a815015c7d1764399215767b674668b7235832
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345116"
---
# <a name="geometry-section"></a>[Geometry] セクション

図形を構成する直線と円弧の頂点の座標を一覧表示する行を格納します。 
  
図形のジオメトリは、複数の [ **geometry** ] セクションで表すことができます。 複数のパスが異なるプロパティ ([画像のクリッピング](clippingpath-cell-foreign-image-info-section.md)パスなど) を持つ場合は、複数のパスが役に立つことがあります。 
  
## <a name="remarks"></a>解説

[ **Geometry** ] セクションには、次の行の種類が含まれます。 詳細については、各行のトピックを参照してください。 
  
|**行**|**説明**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |目的の座標に移動します。  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |座標までの線を描画します。  <br/> |
|[[arcto]](arcto-row-geometry-section.md) <br/> |座標までの真円の弧を描画します。  <br/> |
|[[ellipticalarcto]](ellipticalarcto-row-geometry-section.md) <br/> |座標までの楕円の弧を描画します。  <br/> |
|[[polylineto]](polylineto-row-geometry-section.md) <br/> |座標までのポリラインまたは連続した線を描画します。  <br/> |
|[[nurbsto]](nurbsto-row-geometry-section.md) <br/> |座標に一様でない有理数 (NURBS) を描画します。  <br/> |
|[[splinestart]](splinestart-row-geometry-section.md) <br/> |スプラインを開始します。  <br/> |
|[[splineknot]](splineknot-row-geometry-section.md) <br/> |ノット座標までのスプライン セグメントを描画します。  <br/> |
|[[infiniteline]](infiniteline-row-geometry-section.md) <br/> |1 つの座標から別の座標に無限線を描画します。  <br/> |
|[もう](ellipse-row-geometry-section.md) <br/> |中心座標および長軸/短軸から楕円を描画します。  <br/> |
|[[relcubbezto]](relcubbezto-row-geometry-section.md) <br/> |図形の幅と高さを基準に3次ベジエ曲線を描画します。  <br/> |
|[[relellipticalarcto]](relellipticalarcto-row-geometry-section.md) <br/> |図形の高さと幅を基準にして、座標に楕円の弧を描画します。  <br/> |
|[[rellineto]](rellineto-row-geometry-section.md) <br/> |図形の高さと幅を基準にして、座標に直線を描画します。  <br/> |
|[[relmoveto]](relmoveto-row-geometry-section.md) <br/> |図形の幅と高さを基準にして座標に移動します。  <br/> |
|[[relquadbezto]](relquadbezto-row-geometry-section.md) <br/> |図形の幅と高さを基準にして、2次ベジエ曲線を描画します。  <br/> |
   
このセクションにある行の種類を変更するには、行を右クリックして、ショートカット メニューの [**図形要素の変更**] をクリックします。 
  

