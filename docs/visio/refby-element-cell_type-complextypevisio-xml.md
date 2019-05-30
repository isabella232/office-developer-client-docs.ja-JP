---
title: RefBy 要素 (Cell_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: 図面内のページへの参照を指定します。
ms.openlocfilehash: cb47919a97b8ad42f62bcb1337cd8e6b3596f5ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538313"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>RefBy 要素 (Cell_Type complexType) (Visio XML)

図面内のページへの参照を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |文書 .xml、masters、.master、xml、ページ # .xml、ページ # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell 要素 (操作タグセクション)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形またはページ上のアクションタグに1つのプロパティを定義します。  <br/> |
|[Cell 要素 ([Actions] 行)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |ショートカットメニューまたはアクションタグメニューで、ユーザー設定のコマンドに関連付けられているアクションの1つのプロパティを指定します。  <br/> |
|[Cell 要素 ([ArcTo] 行)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |円弧の x 座標、y 座標、または弧を格納します。  <br/> |
|[Cell 要素 (Character セクション)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |フォント、色、スタイル、大文字/小文字、ベースラインに対する相対位置、またはポイントサイズなど、図形のテキストランの書式設定属性を指定します。  <br/> |
|[Cell 要素 ([Connection] 行)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形上の1つの接続ポイントの x 座標または y 座標、水平方向または垂直方向、または種類を格納します。  <br/> |
|[Cell 要素 ([Controls] 行)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形に定義されている特定のコントロールハンドルのプロパティが含まれています。  <br/> |
|[Cell 要素 ([Ellipse] 行)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |楕円の中心点と楕円上の2つの点の x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 ([EllipticalArcTo] 行)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |楕円の弧の端点の x 座標または y 座標、円弧のコントロールポイントの x 座標または y 座標、x 軸から楕円の長軸までの角度、または楕円の長軸と短軸との比率を格納します。  <br/> |
|[Cell 要素 (フィールドセクション)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |[フィールド] ダイアログ ボックスを使用して図形のテキストに挿入した関数および数式を表示します。  <br/> |
|[Cell 要素 (塗りつぶしグラデーション] セクション)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。  <br/> |
|[Cell 要素 (Geometry セクション)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |[Geometry] セクションを構成する線および円弧に関して、書式設定と動作のプロパティを決定するプロパティを定義します。  <br/> |
|[Cell 要素 ([Hyperlink] 行)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形に関連付けられた、単一のハイパーリンクの情報を格納します。 図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。  <br/> |
|[Cell 要素 ([InfiniteLine] 行)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |無限線上にある2つの点の x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 (Layer セクション)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |ページのレイヤーまたはそのプロパティに1つのプロパティを指定します。  <br/> |
|[Cell 要素 (線のグラデーションのセクション)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |線のグラデーションのグラデーションの分岐点の色、透過性、または位置を含みます。  <br/> |
|[Cell 要素 ([LineTo] 行)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 ([MoveTo] 行)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の最初の頂点に対する x 座標または y 座標を格納します。または、パスを切断した後の最初の頂点の x 座標または y 座標を表します。  <br/> |
|[Cell 要素 ([NURBSTo] 行)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |X 座標または y 座標、2番目のノットの位置、最後の太さの位置、最初のノットの位置、最初の太さの位置、または一様でない有理数 (NURBS) の数式を格納します。  <br/> |
|[Cell 要素 (Paragraph セクション)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |インデント、行間、箇条書き、段落の水平方向の配置など、図形のテキストの段落書式属性を指定します。  <br/> |
|[Cell 要素 ([PolyLineTo] 行)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |ポリラインまたはポリライン式の最後のポイントに対する x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 ([RelCubBezTo] 行)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の幅と高さに相対する3次ベジエ曲線の x 座標または y 座標、図形の幅と高さに相対する曲線の始点のコントロールポイントの x 座標または y 座標、またはコントロールポイントの x 座標または y 座標を格納します。図形の幅と高さを基準にして、曲線の終点の位置を示します。  <br/> |
|[Cell 要素 ([RelEllipticalArcTo] 行)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の幅と高さを基準にした楕円弧の端点の x 座標または y 座標、図形の幅と高さに相対する円弧のコントロールポイントの x 座標または y 座標、x 軸から楕円の長軸までの角度、またはの間の比率を格納します。楕円の主軸と短軸。  <br/> |
|[Cell 要素 (RelLineTo Row)](cell-element-rellineto-rowvisio-xml.md)[Cell](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の幅と高さに相対する直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 ([RelMoveTo] 行)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の最初の頂点に対する x 座標または y 座標、またはパスを切断した後の最初の頂点の x 座標または y 座標を格納します。この値は、図形の高さと幅を基準にしています。  <br/> |
|[Cell 要素 ([Relquadbezto] セクション](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の幅と高さに相対する2次ベジエ曲線の x 座標または y 座標、または図形の幅と高さに相対する曲線のコントロールポイントの x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 (スクラッチセクション)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |他のセルから参照できる数式を入力およびテストするための作業領域を指定します。  <br/> |
|[Cell 要素 (Shape Data セクション](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形データの1つのプロパティを指定します。  <br/> |
|[Cell 要素 ([SplineKnot] 行)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |スプラインのコントロールポイントまたはスプラインのノットの x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 (Ineinestart セクション](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |スプラインの2番目のコントロールポイントに対する x 座標または y 座標、2番目のノット、最初のノット、最後のノット、またはスプラインの角度を格納します。  <br/> |
|[Cell 要素 (Tabs セクション)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形およびスタイルタブの終了位置または配置を制御するプロパティを指定します。  <br/> |
|[Cell 要素 (ユーザー定義セルセクション)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |ユーザーが指定した一連の情報の1つのプロパティ。他のセルとアドオンツールで参照できます。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd: アン Signedint  <br/> |必須  <br/> |図面内のページの ID を指定します。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|T  <br/> |xsd: string  <br/> |必須  <br/> |参照の種類を指定します。  <br/> |Xsd: string 型の値。  <br/> |
   

