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
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538313"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>RefBy 要素 (Cell_Type complexType) (Visio XML)

図面内のページへの参照を指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**名詞空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell 要素 ([操作タグ] セクション)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形またはページ上のアクション タグに 1 つのプロパティを定義します。  <br/> |
|[Cell 要素 ([Actions] 行)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |ショートカットまたはアクション タグ メニューのカスタム コマンドに関連付けられているアクションの1つのプロパティを指定します。  <br/> |
|[Cell 要素 ([ArcTo] 行)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |円弧の x 座標、y 座標、または弓形が含まれます。  <br/> |
|[Cell 要素 ([文字] セクション)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |フォント、色、スタイル、大文字と小文字、ベースラインに相対する位置、またはポイント サイズなどの図形のテキスト実行の書式属性を指定します。  <br/> |
|[Cell 要素 ([Connection] 行)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形上にある単一の接続ポイントに関する、x 座標または y 座標、水平方向または垂直方向、または種類を格納します。  <br/> |
|[Cell 要素 ([Controls] 行)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形に定義された特定のコントロール ハンドルのプロパティが含まれます。  <br/> |
|[Cell 要素 ([Ellipse] 行)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |楕円の中心点および楕円上の 2 つの点に対する x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 ([EllipticalArcTo] 行)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |楕円の弧の端点に対する x 座標または y 座標、円弧のコントロール ポイントに対する x 座標または y 座標、x 軸から楕円の長軸までの角度、または楕円の長軸と短軸との比率を格納します。  <br/> |
|[Cell 要素 ([フィールド] セクション)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |[フィールド] ダイアログ ボックスを使用して、図形のテキストに挿入された関数と数式を表示します。  <br/> |
|[Cell 要素 ([塗りつぶしグラデーション] セクション)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |塗りつぶしグラデーションについて、グラデーションの分岐点の色、透過性、および位置を格納します。  <br/> |
|[Cell 要素 ([図形座標] セクション)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |[図形座標] セクションを構成する線や円弧に関する、書式設定および動作プロパティを決定するプロパティを定義します。  <br/> |
|[Cell 要素 ([Hyperlink] 行)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形に関連付けられた、単一のハイパーリンクの情報を格納します。 図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。  <br/> |
|[Cell 要素 ([InfiniteLine] 行)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |無限線上の 2 つの点に対する x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 ([レイヤー] セクション)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |レイヤーまたはページのプロパティのいずれか 1 つを指定します。  <br/> |
|[Cell 要素 ([線のグラデーション] セクション)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |線のグラデーションについて、グラデーションの分岐点の色、透過性、または位置を格納します。  <br/> |
|[Cell 要素 ([LineTo] 行)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 ([MoveTo] 行)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の最初の頂点に対する x 座標または y 座標を格納します。または、パスを切断した後の最初の頂点に対する x または y 座標を表します。  <br/> |
|[Cell 要素 ([NURBSTo] 行)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |x 座標または y 座標、最後から 2 番目のノットの位置、最後のウェイトの位置、最初のノットの位置、最初のウェイトの位置、または NURBS (nonuniform rational B-spline) の数式を格納します。  <br/> |
|[Cell 要素 ([段落] セクション)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形のテキストに対する、段落の書式属性を指定します。属性には、インデント、行間隔、箇条書き、または段落の水平方向の配置などがあります。  <br/> |
|[Cell 要素 ([PolyLineTo] 行)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |ポリラインの最終ポイントに対する x 座標または y 座標、またはポリライン数式を格納します。  <br/> |
|[Cell 要素 ([RelCubBezTo] 行)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の幅と高さに相対する 3 次ベジエ曲線の端点の x 座標または y 座標、図形の幅と高さに相対する曲線の始点のコントロール ポイントの x 座標または y 座標、または図形の幅と高さに相対する曲線の終点のコントロール ポイントの x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 ([RelEllipticalArcTo] 行)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の幅と高さに相対する楕円の弧の端点に対する x 座標または y 座標、図形の幅と高さに相対する円弧のコントロール ポイントに対する x 座標または y 座標、x 軸から楕円の長軸までの角度、または楕円の長軸と短軸との比率を格納します。  <br/> |
|[Cell 要素 ([RelLineTo] 行)](cell-element-rellineto-rowvisio-xml.md)[Cell](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の幅と高さに相対する、直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 ([RelMoveTo] 行)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の高さおよび幅に相対する、図形の最初の頂点に対する x 座標または y 座標、またはパスを切断した後の最初の頂点に対する x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 ([RelQuadBezTo] 行)](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の幅と高さに相対する 2 次ベジエ曲線のエンドポイントの x 座標または y 座標、または図形の幅と高さに相対する曲線のコントロール ポイントの x 座標または y 座標を格納します。  <br/> |
|[Cell 要素 ([スクラッチ] セクション)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |他のセルが参照する数式の入力およびテストを実行するための作業領域を指定します。  <br/> |
|[Cell 要素 ([図形データ] セクション)](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形データのいずれかのプロパティを指定します。  <br/> |
|[Cell 要素 ([SplineKnot] 行)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |スプラインのコントロール ポイントに対する x 座標または y 座標、またはスプラインのノットを格納します。  <br/> |
|[Cell 要素 ([SplineStart] セクション)](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |スプラインの 2 番目のコントロール ポイントに対するx 座標または y 座標、スプラインの 2 番目のノット、最初のノット、最後のノット、またはスプラインの角度を格納します。  <br/> |
|[Cell 要素 ([タブ] セクション)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形やスタイルのタブ位置または配置を制御するプロパティを指定します。  <br/> |
|[Cell 要素 ([ユーザー定義セル] セクション)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |他のセルおよびアドオン ツールによって参照できる、ユーザー指定の情報の 1 つのプロパティ。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |図面内のページの ID を指定します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|T  <br/> |xsd:string  <br/> |必須  <br/> |参照の種類を指定します。  <br/> |xsd:string 型の値。  <br/> |
   

