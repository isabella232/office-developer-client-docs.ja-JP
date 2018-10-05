---
title: RefBy 要素 (Cell_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: 図面のページへの参照を指定します。
ms.openlocfilehash: 1731bd20a5ba4358c72370dfcdc6d8a6fc791e2f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385859"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>RefBy 要素 (Cell_Type complexType)'Visio XML (')

図面のページへの参照を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml、masters.xml、マスターの # .xml、pages.xml ページ # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell 要素 ([操作タグ] セクション)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形またはページのアクション タグの 1 つのプロパティを定義します。  <br/> |
|[Cell 要素 ([Actions] 行)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |カスタム メニューのコマンドをショートカット メニューまたは操作タグに関連付けられているアクションの 1 つのプロパティを指定します。  <br/> |
|[Cell 要素 ([ArcTo] 行)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |X を含む座標、y 座標、または円弧の弓。  <br/> |
|[Cell 要素 ([文字] セクション)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |フォント、色、スタイル、ケース、ベースラインに相対位置またはポイント サイズなど、図形のテキスト ランの書式設定属性を指定します。  <br/> |
|[Cell 要素 ([Connection] 行)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |X 座標または y 座標、水平方向または垂直方向、または図形の 1 つの接続ポイントの型が含まれています。  <br/> |
|[Cell 要素 ([Controls] 行)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形に対して定義されている特定のコントロール ハンドルのプロパティが含まれています。  <br/> |
|[Cell 要素 ([Ellipse] 行)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |楕円の中心点および楕円上の 2 つの点の x 座標または y 座標が含まれています。  <br/> |
|[Cell 要素 ([EllipticalArcTo] 行)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |X 座標または y 座標、楕円の円弧の終点の x 座標または y 座標のコントロールは、円弧、楕円の長軸、または比率を x 軸から楕円の長軸と短軸の軸間の角度のポイントが含まれます。  <br/> |
|[Cell 要素 ([フィールド] セクション)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |[フィールド] ダイアログ ボックスを使用して図形のテキストに挿入した関数および数式を表示します。  <br/> |
|[Cell 要素 ([塗りつぶしグラデーション] セクション)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。  <br/> |
|[Cell 要素 ([図形座標] セクション)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |直線と円弧 [Geometry] セクションを構成する関連プロパティを書式設定および動作を決定するプロパティを定義します。  <br/> |
|[Cell 要素 ([Hyperlink] 行)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形に関連付けられた、単一のハイパーリンクの情報を格納します。図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。  <br/> |
|[Cell 要素 ([InfiniteLine] 行)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |無限線上の 2 つの点の x 座標または y 座標が含まれています。  <br/> |
|[Cell 要素 ([レイヤー] セクション)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |レイヤーの 1 つのプロパティ ページのプロパティを指定します。  <br/> |
|[Cell 要素 ([線のグラデーション] セクション)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |色や透明度、線のグラデーションのグラデーション ストップの位置が含まれています。  <br/> |
|[Cell 要素 ([LineTo] 行)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |含まれている x のまたは直線の線分の終点の y 座標。  <br/> |
|[Cell 要素 ([MoveTo] 行)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の最初の頂点の x 座標または y 座標が含まれていますか、パス内の改行の後の最初の頂点の x 座標または y 座標を表します。  <br/> |
|[Cell 要素 ([NURBSTo] 行)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |2 番目の最後のノット、最初のウェイトまたは不均一な合理性のある B-スプライン (NURBS) の数式の位置、最初のノットの位置、最後のウェイトの位置の x 座標または y 座標、位置が含まれています。  <br/> |
|[Cell 要素 ([段落] セクション)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |段落のインデント、行間隔、箇条書き、または段落の水平方向の配置などの図形のテキストの属性を指定します。  <br/> |
|[Cell 要素 ([PolyLineTo] 行)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |X 座標または y 座標ポリラインまたはポリラインの数式の最後の点が含まれています。  <br/> |
|[Cell 要素 ([RelCubBezTo] 行)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の幅と高さの 3 次ベジエ曲線の端点、曲線の相対的な図形の幅と高さの最初の制御点の x 座標または y 座標の制御点の x 座標または y 座標の x 座標または y 座標が含まれています曲線の相対的な図形の幅と高さの終了します。  <br/> |
|[Cell 要素 ([RelEllipticalArcTo] 行)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |X 座標または y 座標、図形の幅と高さを基準にして楕円の円弧の端点の基準にして図形の幅と高さ、角度、楕円の長軸、または間の比率を x 軸から円弧上の x 座標または y 座標のコントロール ポイントを含む、楕円の長軸と短軸の軸です。  <br/> |
|[セル要素 (RelLineTo 行)](cell-element-rellineto-rowvisio-xml.md)[セル](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |含まれている x、または図形の幅と高さを基準にして、直線の線分の終点の y 座標。  <br/> |
|[Cell 要素 ([RelMoveTo] 行)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の幅と高さを基準にして、パス内の改行の後、図形の最初の頂点または最初の頂点の x 座標または y 座標の x 座標または y 座標が含まれています。  <br/> |
|[([RelQuadBezTo] セクションのセル要素](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形の幅と高さを基準にして二次ベジェ曲線の端点または曲線の相対的な図形の幅と高さの制御点の x 座標または y 座標の x 座標または y 座標が含まれています。  <br/> |
|[Cell 要素 ([スクラッチ] セクション)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |入力および他のセルを参照する数式をテストするための作業領域を指定します。  <br/> |
|[(図形データ セクションのセル要素](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形データの 1 つのプロパティを指定します。  <br/> |
|[Cell 要素 ([SplineKnot] 行)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |X 座標または y 座標、スプラインの制御点、またはスプラインのノットが含まれています。  <br/> |
|[([A] セクションのセル要素](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |X 座標または y 座標、スプラインの 2 番目の制御点、2 番目のノット、最初のノット、最後のノット、またはスプラインの角度が含まれています。  <br/> |
|[Cell 要素 ([タブ] セクション)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形および [スタイル] タブの停止位置や配置を制御するプロパティを指定します。  <br/> |
|[Cell 要素 ([ユーザー定義セル] セクション)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1 つのプロパティ、ユーザー指定の情報の他のセルやアドオン ツールによって参照できます。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |図面内のページの ID を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|SV 要素  <br/> |xsd:string  <br/> |必須  <br/> |参照型を指定します。  <br/> |Xsd:string の値を入力します。  <br/> |
   

