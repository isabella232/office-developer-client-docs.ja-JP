---
title: セクションの要素 (Sheet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: 関連するプロパティのコレクションを指定します。
ms.openlocfilehash: 7cb5e1c30960e69b252abc7af38e021607fd3502
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806365"
---
# <a name="section-element-sheettype-complextype-visio-xml"></a>セクションの要素 (Sheet_Type complexType)'Visio XML (')

関連するプロパティのコレクションを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml、masters.xml、マスターの # .xml、pages.xml ページ # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |図面のプロパティを指定します。  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |図面ページのプロパティを指定します。  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |マスターに関連付けられている図面ページのプロパティを指定します。  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |図形に関連付けられているプロパティのコレクションを指定します。  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |スタイル、図面、図面ページまたは図形に関連付けられているプロパティのコレクションを指定します。  <br/> |
|[スタイル シート](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |スタイル シートを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](http://msdn.microsoft.com/library/70a9d6d6-a4ff-2b0d-febc-789a04a2f5b0%28Office.15%29.aspx) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1 つのプロパティを指定します。  <br/> |
|[Row](http://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |**Cell_Type**要素のコレクションを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |省略可能  <br/> |継承されるコレクションが削除されたかどうかを指定します。 0 または 1 に等しい場合があります。 1 の値は、コレクションが使用されておらず、無視することを指定します。 0 の値は、プロパティのコレクションは、図形の有効なことを指定します。 **Del**属性が存在しない場合は、値は 0 になります。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |要素の 0 から始まるインデックスを指定します。 **Section_Type**属性を持つ要素の同じ**N**を含む**Sheet_Type**の間で一意でなければなりません。 含まれている**Sheet_Type**の同じ**N**属性を使用して、上記の**Section_Type**要素の**IX**属性よりも大きい場合があります。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|N  <br/> |xsd:string  <br/> |必須  <br/> |プロパティのコレクションの言語に依存しない名前を指定します。 「ジオメトリ」と同じでない限り**Sheet_Type**はコンテナー要素の**Section_Type**要素の間一意でなければなりません。 **セクション**で、小見出しに等しい場合があります。  <br/> |Xsd:string の値を入力します。  <br/> |
   
### <a name="remarks"></a>注釈

この**セクション**の要素の**N**属性は、限られた一連の**シェイプ シート**のセルに対応する値のいずれかである必要があります。 この**セクション**の要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|アクション  <br/> |式の評価に使用されるプロパティのコレクションです。 **ShapeSheet_Type**または**PageSheet_Type**の親要素が必要です。  <br/> |[[Actions] セクション](actions-section.md) <br/> |
|ActionTag  <br/> |数式評価目的のみに使用されるプロパティのコレクションです。 **ShapeSheet_Type**または**PageSheet_Type**の親要素が必要です。  <br/> |[[操作タグ] セクション](action-tag-section.md) <br/> |
|接続  <br/> |数式評価目的のみに使用されるプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。  <br/> ||
|Controls  <br/> |数式評価目的のみに使用されるプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。  <br/> |[[Controls] セクション](controls-section.md) <br/> |
|Hyperlink  <br/> |図形のハイパーリンクを指定する関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。  <br/> |[[Hyperlinks] セクション](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |図形データを指定する関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。  <br/> |[[Shape Data] セクション](shape-data-section.md) <br/> |
|ユーザー  <br/> |式の評価に使用されるプロパティのコレクションです。 **DocumentSheet_Type**、 **PageSheet_Type**、または**ShapeSheet_Type**の親要素が必要です。  <br/> |[[User-defined Cells] セクション](user-defined-cells-section.md) <br/> |
   
**IX**この要素の属性 **] セクション**は、限られた**シェイプ シート**のセルに対応する値のいずれかである必要があります。 この**セクション**の要素に対して許可されている**IX**属性の値を決定するのには次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|Annotation  <br/> |ドキュメントのページに挿入されたコメントについての情報を格納するプロパティのコレクションです。  <br/> |[[Annotation] セクション](annotation-section.md) <br/> |
|文字  <br/> |図形のテキストの文字のプロパティを指定する関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素または**StyleSheet_Type**の親要素が必要です。  <br/> |[[Character] セクション](character-section.md) <br/> |
|接続  <br/> |数式評価目的のみに使用されるプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。  <br/> |[[Connection Points] セクション](connection-points-section.md) <br/> |
|フィールド  <br/> |図形のテキスト フィールドを指定する関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。  <br/> |[[Text Fields] セクション](text-fields-section.md) <br/> |
|FillGradient  <br/> |図形の塗りつぶしの色のグラデーションを指定するプロパティのコレクションです。 **ShapeSheet_Type**または**StyleSheet_Type**の親要素が必要です。  <br/> |[[塗りつぶしグラデーション] セクション](fill-gradient-section.md) <br/> |
|Geometry  <br/> |ジオメトリの視覚化を指定する関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。 この要素の**Row_Type**の最初の子要素は、[moveto]、RelMoveTo、楕円、または InfiniteLine の型でなければなりません。  <br/> |[[Geometry] セクション](geometry-section.md) <br/> |
|Layers  <br/> |図面ページで定義されているすべてのレイヤーを表示するプロパティのコレクションです。 **PageSheet_Type**要素の子である必要があります。  <br/> |[[Layers] セクション](layers-section.md) <br/> |
|線のグラデーション  <br/> |図形の線の色のグラデーションを指定する関連するプロパティのコレクションです。 **ShapeSheet_Type**または**StyleSheet_Type**の親要素が必要です。  <br/> |[[線のグラデーション] セクション](line-gradient-section.md) <br/> |
|段落  <br/> |図形のテキストの段落のプロパティを指定する関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素または**StyleSheet_Type**の親要素が必要です。  <br/> |[[Paragraph] セクション](paragraph-section.md) <br/> |
|Reviewer  <br/> |式の評価に使用されるプロパティのコレクションです。 **DocumentSheet_Type**の親要素が必要です。  <br/> |[[Reviewer] セクション](reviewer-section.md) <br/> |
|スクラッチ  <br/> |式の評価に使用されるプロパティのコレクションです。 **DocumentSheet_Type**、 **PageSheet_Type**、または**ShapeSheet_Type**の親要素が必要です。  <br/> |[[Scratch] セクション](scratch-section.md) <br/> |
|タブ  <br/> |図形のテキストのタブのプロパティを指定する関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素または**StyleSheet_Type**の親要素が必要です。  <br/> |[[Tabs] セクション](tabs-section.md) <br/> |
   

