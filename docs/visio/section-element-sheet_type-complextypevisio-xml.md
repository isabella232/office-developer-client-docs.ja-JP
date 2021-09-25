---
title: Section 要素 (Sheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: 関連するプロパティのコレクションを指定します。
ms.openlocfilehash: c2d6fdcb39bd99f3ea6bb564794f068dd98e34cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598158"
---
# <a name="section-element-sheet_type-complextype-visio-xml"></a>Section 要素 (Sheet_Type complexType) (Visio XML)

関連するプロパティのコレクションを指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |図面のプロパティを指定します。  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |図面内のページのプロパティを指定します。  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |マスターに関連付けられた図面ページのプロパティを指定します。  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |図形に関連付けられたプロパティのコレクションを指定します。  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |スタイル、図面、図面ページ、図形に関連付けられたプロパティのコレクションを指定します。  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |スタイル シートを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1 つのプロパティを指定します。  <br/> |
|[Row](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |要素のコレクションを **Cell_Type** します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |省略可能  <br/> |それ以外の場合は継承されるコレクションが削除されたかどうかを指定します。 0 または 1 に等しい必要があります。 値 1 は、コレクションが使用され、無視する必要がある場合に指定します。 値 0 は、プロパティのコレクションが図形に対して有効な値を指定します。 Del 属性 **が** 存在しない場合、値は 0 です。  <br/> |xsd:boolean 型の値。  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |要素の 0 から始るインデックスを指定します。 含まれている要素の同じ **N** 属性を持Section_Type要素の中で一意である **必要Sheet_Type。** 含まれている要素の同じ **N** 属性を持Section_Type前の要素の **IX** 属性より大きいSheet_Type。   <br/> |xsd:unsignedInt 型の値。  <br/> |
|N  <br/> |xsd:string  <br/> |必須  <br/> |プロパティのコレクションの言語に依存しない名前を指定します。 "Geometry" に等しくない限り、Section_Type要素のすべての要素Sheet_Type一意である必要があります。 Sections のサブヘッドと等しく **する必要があります**。  <br/> |xsd:string 型の値。  <br/> |
   
### <a name="remarks"></a>注釈

この **Section 要素** の N 属性は **、ShapeSheet** セルに対応する制限された値のセット **の 1 つである必要** があります。 この Section 要素で許可されている **N** 属性の値を決定するには、以下の表を **参照** してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|アクション  <br/> |数式の評価に使用されるプロパティのコレクション。 この要素には、親 **ShapeSheet_Type** または **PageSheet_Type** する必要があります。  <br/> |[[Actions] セクション](actions-section.md) <br/> |
|ActionTag  <br/> |数式の評価にのみ使用されるプロパティのコレクション。 この要素には、親 **ShapeSheet_Type** または **PageSheet_Type** する必要があります。  <br/> |[[操作タグ] セクション](action-tag-section.md) <br/> |
|接続  <br/> |数式の評価にのみ使用されるプロパティのコレクション。 この要素には、親 **ShapeSheet_Type** 必要があります。  <br/> ||
|コントロール  <br/> |数式の評価にのみ使用されるプロパティのコレクション。 この要素には、親 **ShapeSheet_Type** 必要があります。  <br/> |[[Controls] セクション](controls-section.md) <br/> |
|Hyperlink  <br/> |図形のハイパーリンクを指定する関連プロパティのコレクション。 この要素には、親 **ShapeSheet_Type** 必要があります。  <br/> |[[Hyperlinks] セクション](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |図形データを指定する関連プロパティのコレクション。 この要素には、親 **ShapeSheet_Type** 必要があります。  <br/> |[[Shape Data] セクション](shape-data-section.md) <br/> |
|ユーザー  <br/> |数式の評価に使用されるプロパティのコレクション。 この要素には、親DocumentSheet_Type、PageSheet_Type、**またはShapeSheet_Type** する必要があります。  <br/> |[[User-defined Cells] セクション](user-defined-cells-section.md) <br/> |
   
この **Section 要素** の IX 属性は **、ShapeSheet** セルに対応する制限された値のセット **の 1 つである必要** があります。 次の表を参照して、この Section 要素で許可される **IX** 属性の値を **決定** します。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|Annotation  <br/> |ドキュメント ページに挿入されたコメントに関する情報を含むプロパティのコレクション。  <br/> |[[Annotation] セクション](annotation-section.md) <br/> |
|文字  <br/> |図形のテキストの文字プロパティを指定する関連プロパティのコレクション。 親要素または親 **ShapeSheet_Type****要素をStyleSheet_Type** する必要があります。  <br/> |[[Character] セクション](character-section.md) <br/> |
|接続  <br/> |数式の評価にのみ使用されるプロパティのコレクション。 この要素には、親 **ShapeSheet_Type** 必要があります。  <br/> |[[Connection Points] セクション](connection-points-section.md) <br/> |
|フィールド  <br/> |図形のテキスト フィールドを指定する関連プロパティのコレクション。 この要素には、親 **ShapeSheet_Type** 必要があります。  <br/> |[[Text Fields] セクション](text-fields-section.md) <br/> |
|FillGradient  <br/> |図形の塗りつぶしの色のグラデーションを指定するプロパティのコレクション。 この要素には、親 **ShapeSheet_Type** または **StyleSheet_Type** する必要があります。  <br/> |[[塗りつぶしのグラデーション] セクション](fill-gradient-section.md) <br/> |
|Geometry  <br/> |ジオメトリの視覚エフェクトを指定する関連プロパティのコレクション。 この要素には、親 **ShapeSheet_Type** 必要があります。 この要素 **Row_Type** 子要素の最初の要素は、MoveTo、RelMoveTo、楕円、または InfiniteLine 型である必要があります。  <br/> |[[Geometry] セクション](geometry-section.md) <br/> |
|Layers  <br/> |図面ページで定義されているすべてのレイヤーを表示するプロパティのコレクション。 これは、要素の子 **PageSheet_Type** 必要があります。  <br/> |[[Layers] セクション](layers-section.md) <br/> |
|線のグラデーション  <br/> |図形の線の色のグラデーションを指定する関連プロパティのコレクション。 この要素には、親 **ShapeSheet_Type** または **StyleSheet_Type** する必要があります。  <br/> |[[線のグラデーション] セクション](line-gradient-section.md) <br/> |
|Paragraph  <br/> |図形のテキストの段落プロパティを指定する関連プロパティのコレクション。 親要素または親 **ShapeSheet_Type****要素をStyleSheet_Type** する必要があります。  <br/> |[[Paragraph] セクション](paragraph-section.md) <br/> |
|レビュー担当者  <br/> |数式の評価に使用されるプロパティのコレクション。 この要素には、親 **DocumentSheet_Type** 必要があります。  <br/> |[[Reviewer] セクション](reviewer-section.md) <br/> |
|Scratch  <br/> |数式の評価に使用されるプロパティのコレクション。 この要素には、親DocumentSheet_Type、PageSheet_Type、**またはShapeSheet_Type** する必要があります。  <br/> |[[Scratch] セクション](scratch-section.md) <br/> |
|タブ  <br/> |図形のテキストのタブ プロパティを指定する関連プロパティのコレクション。 親要素または親 **ShapeSheet_Type****要素をStyleSheet_Type** する必要があります。  <br/> |[[Tabs] セクション](tabs-section.md) <br/> |
   

