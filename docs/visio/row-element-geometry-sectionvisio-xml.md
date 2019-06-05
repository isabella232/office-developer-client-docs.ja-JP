---
title: Row 要素 (Geometry セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: 図形を構成する直線と円弧の頂点の座標を一覧表示する行を格納します。
ms.openlocfilehash: 6dbf18b749ed072645c4941922729010f74fc0ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540855"
---
# <a name="row-element-geometry-section-visio-xml"></a>Row 要素 (Geometry セクション) (Visio XML)

図形を構成する直線と円弧の頂点の座標を一覧表示する行を格納します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |マスター # .xml、ページ # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Row" type="GeometryRow_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |図形を構成する直線と円弧の頂点の座標を一覧表示する行を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

> [!NOTE]
> Cell 要素は、この要素の唯一の子です。 この要素の "T" 属性によって、Cell 要素の意味は異なります。 次の表では、要素名の parathetical テキストは、トピックが適用される "T" 値に対応しています。 
  
|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell 要素 ([ArcTo] 行)](arcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |円弧の x 座標と y 座標、および弧を格納します。  <br/> |
|[Cell 要素 ([Ellipse] 行)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |楕円の中心点および楕円上の 2 つの点に対する x 座標と y 座標を格納します。  <br/> |
|[Cell 要素 ([EllipticalArcTo] 行)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |楕円の弧の端点に対する x 座標と y 座標、円弧のコントロール ポイントに対する x 座標と y 座標、x 軸から楕円の長軸までの角度、および楕円の長軸と短軸との比率を格納します。  <br/> |
|[Cell 要素 ([InfiniteLine] 行)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |無限線上の 2 つの点に対する x 座標と y 座標を格納します。  <br/> |
|[Cell 要素 ([LineTo] 行)](lineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |直線セグメントの最後の頂点に対する x 座標および y 座標を格納します。  <br/> |
|[Cell 要素 ([MoveTo] 行)](moveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |図形の最初の頂点に対する x 座標および y 座標を格納します。または、パスを切断した後の最初の頂点に対する x および y 座標を表します。  <br/> |
|[Cell 要素 ([NURBSTo] 行)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |x 座標と y 座標、最後から 2 番目のノットの位置、最後のウェイトの位置、最初のノットの位置、最初のウェイトの位置、および NURBS (nonuniform rational B-spline) の数式を格納します。  <br/> |
|[Cell 要素 ([PolyLineTo] 行)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |ポリラインの最終ポイントに対する x 座標と y 座標、およびポリライン数式を格納します。  <br/> |
|[Cell 要素 ([RelCubBezTo] 行)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |図形の幅と高さを基準にした3次ベジエ曲線の x 座標と y 座標、図形の幅と高さに相対する曲線の始点のコントロールポイントの x 座標および y 座標、およびコントロールの x 座標および y 座標を格納しています。図形の幅と高さを基準にして、曲線の終点の点を指定します。  <br/> |
|[Cell 要素 ([RelQuadBezTo] 行)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |図形の幅と高さに相対する2次ベジエ曲線の x 座標と y 座標、および図形の幅と高さに相対する曲線のコントロールポイントの x 座標と y 座標を格納します。  <br/> |
|[Cell 要素 ([RelEllipticalArcTo] 行)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |図形の幅と高さに相対する円弧の端点の x 座標と y 座標、図形の幅と高さに相対する円弧のコントロールポイントの x 座標と y 座標、x 軸から楕円の長軸までの角度、およびその間の比率を格納します。楕円の主軸と短軸。  <br/> |
|[Cell 要素 ([RelLineTo] 行)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |図形の幅と高さに相対する直線セグメントの最後の頂点に対する x 座標と y 座標を格納します。  <br/> |
|[Cell 要素 ([RelMoveTo] 行)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |図形の高さおよび幅に相対する、図形の最初の頂点に対する x 座標および y 座標、またはパスを切断した後の最初の頂点に対する x 座標および y 座標を格納します。  <br/> |
|[Cell 要素 ([RelQuadBezTo] 行)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |図形の幅と高さに相対する2次ベジエ曲線の x 座標と y 座標、および図形の幅と高さに相対する曲線のコントロールポイントの x 座標と y 座標を格納します。  <br/> |
|[Cell 要素 ([SplineKnot] 行)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |スプラインのコントロール ポイントに対する x 座標と y 座標、およびスプラインのノットを格納します。  <br/> |
|[Cell 要素 ([SplineStart] 行)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |スプラインの 2 番目のコントロール ポイントに対するx 座標と y 座標、スプラインの 2 番目のノット、最初のノット、最後のノット、およびスプラインの角度を格納します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd: boolean  <br/> |省略可能  <br/> |マスターシェイプから継承される行が削除されているかどうかを指定します。  <br/> |Xsd: boolean 型の値。  <br/> |
|IX  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |行の1から始まる識別子を指定します。 これは、同じセクションの他の識別子よりも大きい qiue-v である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、スクラッチ、およびタブセクションにのみ使用されます。 行には、IX 属性または N 属性のいずれかのみを含めることができます。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|LocalName  <br/> |xsd: string  <br/> |省略可能  <br/> |行の一意の言語に依存する名前を指定します。  <br/> |Xsd: string 型の値。  <br/> |
|N  <br/> |xsd: string  <br/> |省略可能  <br/> |一意の言語に依存しない行の名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、および ActionTag セクションにのみ使用されます。 行には、IX 属性または N 属性のいずれかのみを含めることができます。  <br/> |Xsd: string 型の値。  <br/> |
|T  <br/> |xsd: string  <br/> |省略可能  <br/> |Geometry の視覚化で使用される、行で表されるジオメトリックパスの種類を指定します。 T 属性は、[Geometry] セクションにのみ使用されます。  <br/> |Xsd: string 型の値。  <br/> |
   
## <a name="remarks"></a>解説

この**Row**要素の**T**属性は、シェイプシートの行に対応する、制限された値のセットのいずれかである必要があります。 この**Row**要素に使用できる**T**属性の値を確認するには、次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|[Arcto]  <br/> |円弧の x 座標と y 座標、および弧を格納します。  <br/> |[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md) <br/> |
|もう  <br/> |楕円の中心点および楕円上の 2 つの点に対する x 座標と y 座標を格納します。  <br/> |[[Ellipse] 行 ([Geometry] セクション)](ellipse-row-geometry-section.md) <br/> |
|[Ellipticalarcto]  <br/> |楕円の弧の端点に対する x 座標と y 座標、円弧のコントロール ポイントに対する x 座標と y 座標、x 軸から楕円の長軸までの角度、および楕円の長軸と短軸との比率を格納します。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
|[Infiniteline]  <br/> |無限線上の 2 つの点に対する x 座標と y 座標を格納します。  <br/> |[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md) |
|LineTo  <br/> |直線セグメントの最後の頂点に対する x 座標および y 座標を格納します。  <br/> |[[LineTo] 行 ([Geometry] セクション)](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |図形の最初の頂点に対する x 座標および y 座標を格納します。または、パスを切断した後の最初の頂点に対する x および y 座標を表します。  <br/> |[[MoveTo] 行 ([Geometry] セクション)](moveto-row-geometry-section.md) <br/> |
|[Nurbsto]  <br/> |x 座標と y 座標、最後から 2 番目のノットの位置、最後のウェイトの位置、最初のノットの位置、最初のウェイトの位置、および NURBS (nonuniform rational B-spline) の数式を格納します。  <br/> |[[NURBSTo] 行 ([Geometry] セクション)](nurbsto-row-geometry-section.md) <br/> |
|[Polylineto]  <br/> |ポリラインの最終ポイントに対する x 座標と y 座標、およびポリライン数式を格納します。  <br/> |[[PolylineTo] 行 ([Geometry] セクション)](polylineto-row-geometry-section.md) <br/> |
|[Relcubbezto]  <br/> |図形の幅と高さを基準にした3次ベジエ曲線の x 座標と y 座標、図形の幅と高さに相対する曲線の始点のコントロールポイントの x 座標および y 座標、およびコントロールの x 座標および y 座標を格納しています。図形の幅と高さを基準にして、曲線の終点の点を指定します。  <br/> |[[Relcubbezto] 行 (Geometry セクション)](relcubbezto-row-geometry-section.md) <br/> |
|[Relellipticalarcto]  <br/> |図形の幅と高さに相対する円弧の端点の x 座標と y 座標、図形の幅と高さに相対する円弧のコントロールポイントの x 座標と y 座標、x 軸から楕円の長軸までの角度、およびその間の比率を格納します。楕円の主軸と短軸。  <br/> |[[Relellipticalarcto] 行 (Geometry セクション)](relellipticalarcto-row-geometry-section.md) <br/> |
|[Rellineto]  <br/> |図形の幅と高さに相対する直線セグメントの最後の頂点に対する x 座標と y 座標を格納します。  <br/> |[RelLineTo 行 (図形座標] セクション)](rellineto-row-geometry-section.md) <br/> |
|[Relmoveto]  <br/> |図形の高さおよび幅に相対する、図形の最初の頂点に対する x 座標および y 座標、またはパスを切断した後の最初の頂点に対する x 座標および y 座標を格納します。  <br/> |[「RelMoveTo」行 (「Geometry」セクション)](relmoveto-row-geometry-section.md) <br/> |
|[Relquadbezto]  <br/> |図形の幅と高さに相対する2次ベジエ曲線の x 座標と y 座標、および図形の幅と高さに相対する曲線のコントロールポイントの x 座標と y 座標を格納します。  <br/> |[[Relquadbezto] 行 (Geometry セクション)](relquadbezto-row-geometry-section.md) <br/> |
|[Splineknot]  <br/> |スプラインのコントロール ポイントに対する x 座標と y 座標、およびスプラインのノットを格納します。  <br/> |[[SplineKnot] 行 ([Geometry] セクション)](splineknot-row-geometry-section.md) <br/> |
|[Splinestart]  <br/> |スプラインの 2 番目のコントロール ポイントに対するx 座標と y 座標、スプラインの 2 番目のノット、最初のノット、最後のノット、およびスプラインの角度を格納します。  <br/> |[[SplineStart] 行 ([Geometry] セクション)](splinestart-row-geometry-section.md) <br/> |
   

