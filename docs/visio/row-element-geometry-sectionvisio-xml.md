---
title: 行要素 ([Geometry] セクション) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: 直線と図形を構成する円弧の頂点の座標を一覧表示する行が含まれています。
ms.openlocfilehash: 7a829651c4cab62a5c583d068211b9ffa20e725e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806283"
---
# <a name="row-element-geometry-section-visio-xml"></a>行要素 ([Geometry] セクション) ('Visio XML')

直線と図形を構成する円弧の頂点の座標を一覧表示する行が含まれています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |# .xml をマスター、# .xml のページ  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Row" type="GeometryRow_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[セクション](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |直線と図形を構成する円弧の頂点の座標を一覧表示する行が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

> [!NOTE]
> セル要素は、この要素の唯一の子です。 この要素の"T"属性によって、セル要素の意味が異なります。 次の表では、parathetical テキストを要素名では、トピックを適用する"T"の値に対応しています。 
  
|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell 要素 ([ArcTo] 行)](arcto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |円弧の x 座標と y 座標、および弧を格納します。  <br/> |
|[Cell 要素 ([Ellipse] 行)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |楕円の中心点および楕円上の 2 つの点に対する x 座標と y 座標を格納します。  <br/> |
|[Cell 要素 ([EllipticalArcTo] 行)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |楕円の弧の端点に対する x 座標と y 座標、円弧のコントロール ポイントに対する x 座標と y 座標、x 軸から楕円の長軸までの角度、および楕円の長軸と短軸との比率を格納します。  <br/> |
|[Cell 要素 ([InfiniteLine] 行)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |無限線上の 2 つの点に対する x 座標と y 座標を格納します。  <br/> |
|[Cell 要素 ([LineTo] 行)](lineto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |直線セグメントの最後の頂点に対する x 座標および y 座標を格納します。  <br/> |
|[Cell 要素 ([MoveTo] 行)](moveto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |図形の最初の頂点に対する x 座標および y 座標を格納します。または、パスを切断した後の最初の頂点に対する x および y 座標を表します。  <br/> |
|[Cell 要素 ([NURBSTo] 行)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |x 座標と y 座標、最後から 2 番目のノットの位置、最後のウェイトの位置、最初のノットの位置、最初のウェイトの位置、および NURBS (nonuniform rational B-spline) の数式を格納します。  <br/> |
|[Cell 要素 ([PolyLineTo] 行)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |ポリラインの最終ポイントに対する x 座標と y 座標、およびポリライン数式を格納します。  <br/> |
|[Cell 要素 ([RelCubBezTo] 行)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |図形の幅と高さの 3 次ベジエ曲線の端点、曲線の相対的な図形の幅と高さの先頭と、コントロールの x 座標と y 座標の制御点の x 座標と y 座標の x 座標と y 座標が含まれています曲線の相対的な図形の幅と高さの最後のポイントです。  <br/> |
|[Cell 要素 ([RelQuadBezTo] 行)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |図形の幅と高さを基準にして二次ベジェ曲線の端点と曲線の相対的な図形の幅と高さの制御点の x 座標と y 座標の x 座標と y 座標が含まれています。  <br/> |
|[Cell 要素 ([RelEllipticalArcTo] 行)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |X 座標と y 座標、図形の幅と高さを基準にして楕円の円弧の終点の x 座標と y 座標図形の幅と高さ、角度は、x 軸から楕円の長軸との比率を基準にして円弧のコントロール ポイントにはが含まれます楕円の長軸と短軸の軸です。  <br/> |
|[Cell 要素 ([RelLineTo] 行)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |含まれています x、および図形の幅と高さを基準にして、直線の線分の終点の y 座標。  <br/> |
|[Cell 要素 ([RelMoveTo] 行)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |図形の高さおよび幅に相対する、図形の最初の頂点に対する x 座標および y 座標、またはパスを切断した後の最初の頂点に対する x 座標および y 座標を格納します。  <br/> |
|[Cell 要素 ([RelQuadBezTo] 行)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |図形の幅と高さを基準にして二次ベジェ曲線の端点と曲線の相対的な図形の幅と高さの制御点の x 座標と y 座標の x 座標と y 座標が含まれています。  <br/> |
|[Cell 要素 ([SplineKnot] 行)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |スプラインのコントロール ポイントに対する x 座標と y 座標、およびスプラインのノットを格納します。  <br/> |
|[Cell 要素 ([SplineStart] 行)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |スプラインの 2 番目のコントロール ポイントに対するx 座標と y 座標、スプラインの 2 番目のノット、最初のノット、最後のノット、およびスプラインの角度を格納します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |省略可能  <br/> |マスター シェイプから継承される行が削除されたかどうかを指定します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |1 から始まる行の識別子を指定します。 特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。 行は、IX または N の属性の 1 つだけ配置できます。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|LocalName  <br/> |xsd:string  <br/> |省略可能  <br/> |行の一意の言語に依存する名前を指定します。  <br/> |Xsd:string の値を入力します。  <br/> |
|N  <br/> |xsd:string  <br/> |省略可能  <br/> |行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。 行は、IX または N の属性の 1 つだけ配置できます。  <br/> |Xsd:string の値を入力します。  <br/> |
|SV 要素  <br/> |xsd:string  <br/> |省略可能  <br/> |行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。 T 属性は、[Geometry] セクションでのみ使用します。  <br/> |Xsd:string の値を入力します。  <br/> |
   
## <a name="remarks"></a>注釈

**T**この要素の属性**の行**は、限られた一連のシェイプ シート行に対応する値のいずれかである必要があります。 この**行**の要素に対して許可されている**T**属性の値を決定するのには次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|ArcTo  <br/> |円弧の x 座標と y 座標、および弧を格納します。  <br/> |[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md) <br/> |
|楕円  <br/> |楕円の中心点および楕円上の 2 つの点に対する x 座標と y 座標を格納します。  <br/> |[[Ellipse] 行 ([Geometry] セクション)](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |楕円の弧の端点に対する x 座標と y 座標、円弧のコントロール ポイントに対する x 座標と y 座標、x 軸から楕円の長軸までの角度、および楕円の長軸と短軸との比率を格納します。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |無限線上の 2 つの点に対する x 座標と y 座標を格納します。  <br/> |[[InfiniteLine] 行 ([Geometry] セクション)](http://msdn.microsoft.com/library/Contains the x- and y-coordinates of two points on an infinite line.%28Office.15%29.aspx) <br/> |
|[Lineto]  <br/> |直線セグメントの最後の頂点に対する x 座標および y 座標を格納します。  <br/> |[[LineTo] 行 ([Geometry] セクション)](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |図形の最初の頂点に対する x 座標および y 座標を格納します。または、パスを切断した後の最初の頂点に対する x および y 座標を表します。  <br/> |[[MoveTo] 行 ([Geometry] セクション)](moveto-row-geometry-section.md) <br/> |
|[Nurbsto]  <br/> |x 座標と y 座標、最後から 2 番目のノットの位置、最後のウェイトの位置、最初のノットの位置、最初のウェイトの位置、および NURBS (nonuniform rational B-spline) の数式を格納します。  <br/> |[[NURBSTo] 行 ([Geometry] セクション)](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |ポリラインの最終ポイントに対する x 座標と y 座標、およびポリライン数式を格納します。  <br/> |[[PolylineTo] 行 ([Geometry] セクション)](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |図形の幅と高さの 3 次ベジエ曲線の端点、曲線の相対的な図形の幅と高さの先頭と、コントロールの x 座標と y 座標の制御点の x 座標と y 座標の x 座標と y 座標が含まれています曲線の相対的な図形の幅と高さの最後のポイントです。  <br/> |[[RelCubBezTo] 行 ([図形座標] セクション)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |X 座標と y 座標、図形の幅と高さを基準にして楕円の円弧の終点の x 座標と y 座標図形の幅と高さ、角度は、x 軸から楕円の長軸との比率を基準にして円弧のコントロール ポイントにはが含まれます楕円の長軸と短軸の軸です。  <br/> |[[RelEllipticalArcTo] 行 ([図形座標] セクション)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |含まれています x、および図形の幅と高さを基準にして、直線の線分の終点の y 座標。  <br/> |[[RelLineTo] 行 ([図形座標] セクション)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |図形の高さおよび幅に相対する、図形の最初の頂点に対する x 座標および y 座標、またはパスを切断した後の最初の頂点に対する x 座標および y 座標を格納します。  <br/> |[[RelMoveTo] 行 ([図形座標] セクション)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |図形の幅と高さを基準にして二次ベジェ曲線の端点と曲線の相対的な図形の幅と高さの制御点の x 座標と y 座標の x 座標と y 座標が含まれています。  <br/> |[[RelQuadBezTo] 行 ([図形座標] セクション)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |スプラインのコントロール ポイントに対する x 座標と y 座標、およびスプラインのノットを格納します。  <br/> |[[SplineKnot] 行 ([Geometry] セクション)](splineknot-row-geometry-section.md) <br/> |
|[A  <br/> |スプラインの 2 番目のコントロール ポイントに対するx 座標と y 座標、スプラインの 2 番目のノット、最初のノット、最後のノット、およびスプラインの角度を格納します。  <br/> |[[SplineStart] 行 ([Geometry] セクション)](splinestart-row-geometry-section.md) <br/> |
   

