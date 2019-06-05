---
title: Section 要素 (Sheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: 関連するプロパティのコレクションを指定します。
ms.openlocfilehash: 2862d2ccf10d235996c2a6fb26691d498bdfdbcf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539034"
---
# <a name="section-element-sheettype-complextype-visio-xml"></a>Section 要素 (Sheet_Type complexType) (Visio XML)

関連するプロパティのコレクションを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |文書 .xml、masters、.master、xml、ページ # .xml、ページ # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |図面のプロパティを指定します。  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |図面内のページのプロパティを指定します。  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |マスターシェイプに関連付けられている図面ページのプロパティを指定します。  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |図形に関連付けられたプロパティのコレクションを指定します。  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |スタイル、図面、図面ページ、または図形に関連付けられたプロパティのコレクションを指定します。  <br/> |
|[Xsl](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |スタイルシートを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1つのプロパティを指定します。  <br/> |
|[行](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |**Cell_Type**要素のコレクションを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd: boolean  <br/> |省略可能  <br/> |継承可能なコレクションが削除されているかどうかを指定します。 0または1の値を指定する必要があります。 値が1の場合、コレクションは使用されないため、無視する必要があります。 値0は、プロパティのコレクションが図形に対して有効であることを示します。 **Del**属性が存在しない場合、値は0になります。  <br/> |Xsd: boolean 型の値。  <br/> |
|IX  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |要素の0から始まるインデックスを指定します。 これは、を含む**Sheet_Type**の同じ**N**属性を持つすべての**Section_Type**要素の間で一意である必要があります。 この値は、それを含む**Sheet_Type**の同じ**N**属性を持つ、前の**Section_Type**要素の**IX**属性よりも大きくなければなりません。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|N  <br/> |xsd: string  <br/> |必須  <br/> |プロパティのコレクションの言語に依存しない名前を指定します。 この値は、"Geometry" と同じでない限り、含まれる**Sheet_Type**要素のすべての**Section_Type**要素の中で一意である必要があります。 **セクション**の小見出しと同じである必要があります。  <br/> |Xsd: string 型の値。  <br/> |
   
### <a name="remarks"></a>解説

この**セクション**要素の**N**属性は、**シェイプシート**のセルに対応する、制限された値のセットのいずれかである必要があります。 この**セクション**要素に使用できる**N**属性の値を確認するには、次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|アクション  <br/> |数式の評価に使用されるプロパティのコレクションです。 **ShapeSheet_Type**または**PageSheet_Type**の親要素を指定する必要があります。  <br/> |[[Actions] セクション](actions-section.md) <br/> |
|ActionTag  <br/> |数式の評価のみに使用されるプロパティのコレクションです。 **ShapeSheet_Type**または**PageSheet_Type**の親要素を指定する必要があります。  <br/> |[[操作タグ] セクション](action-tag-section.md) <br/> |
|Connections  <br/> |数式の評価のみに使用されるプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。  <br/> ||
|コントロール  <br/> |数式の評価のみに使用されるプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。  <br/> |[[Controls] セクション](controls-section.md) <br/> |
|Hyperlink  <br/> |図形のハイパーリンクを指定する、関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。  <br/> |[[Hyperlinks] セクション](hyperlinks-section.md) <br/> |
|図形データ  <br/> |図形データを指定する、関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。  <br/> |[[Shape Data] セクション](shape-data-section.md) <br/> |
|ユーザー  <br/> |数式の評価に使用されるプロパティのコレクションです。 **DocumentSheet_Type**、 **PageSheet_Type**、または**ShapeSheet_Type**の親要素を指定する必要があります。  <br/> |[[User-defined Cells] セクション](user-defined-cells-section.md) <br/> |
   
この**セクション**要素の**IX**属性は、**シェイプシート**のセルに対応する、制限された値のセットのいずれかである必要があります。 この**セクション**要素に許可されている**IX**属性の値を確認するには、次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|アノテーションフィーチャー  <br/> |ドキュメントページに挿入されたコメントに関する情報を含むプロパティのコレクションです。  <br/> |[[Annotation] セクション](annotation-section.md) <br/> |
|文字  <br/> |図形のテキストの文字プロパティを指定する、関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素または**StyleSheet_Type**の親要素を指定する必要があります。  <br/> |[[Character] セクション](character-section.md) <br/> |
|Connections  <br/> |数式の評価のみに使用されるプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。  <br/> |[[Connection Points] セクション](connection-points-section.md) <br/> |
|Field  <br/> |図形のテキストフィールドを指定する、関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素が必要です。  <br/> |[[Text Fields] セクション](text-fields-section.md) <br/> |
|FillGradient  <br/> |図形の塗りつぶしの色のグラデーションを指定するプロパティのコレクションです。 **ShapeSheet_Type**または**StyleSheet_Type**の親要素を指定する必要があります。  <br/> |[塗りつぶしのグラデーションセクション](fill-gradient-section.md) <br/> |
|Geometry  <br/> |図形の視覚化を指定する、関連するプロパティのコレクション。 **ShapeSheet_Type**の親要素が必要です。 この要素の最初の**Row_Type**子要素は、Moveto、Relmoveto、楕円、または [infiniteline] の種類である必要があります。  <br/> |[[Geometry] セクション](geometry-section.md) <br/> |
|Layers  <br/> |図面ページに定義されているすべてのレイヤーを表示するプロパティのコレクションです。 **PageSheet_Type**要素の子である必要があります。  <br/> |[[Layers] セクション](layers-section.md) <br/> |
|線のグラデーション  <br/> |図形の線の色のグラデーションを指定する、関連するプロパティのコレクションです。 **ShapeSheet_Type**または**StyleSheet_Type**の親要素を指定する必要があります。  <br/> |[線のグラデーションセクション](line-gradient-section.md) <br/> |
|段落  <br/> |図形のテキストの段落プロパティを指定する、関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素または**StyleSheet_Type**の親要素を指定する必要があります。  <br/> |[[Paragraph] セクション](paragraph-section.md) <br/> |
|レビュー担当者  <br/> |数式の評価に使用されるプロパティのコレクションです。 **DocumentSheet_Type**の親要素が必要です。  <br/> |[[Reviewer] セクション](reviewer-section.md) <br/> |
|仮想  <br/> |数式の評価に使用されるプロパティのコレクションです。 **DocumentSheet_Type**、 **PageSheet_Type**、または**ShapeSheet_Type**の親要素を指定する必要があります。  <br/> |[[Scratch] セクション](scratch-section.md) <br/> |
|タブ  <br/> |図形のテキストの tabs プロパティを指定する、関連するプロパティのコレクションです。 **ShapeSheet_Type**の親要素または**StyleSheet_Type**の親要素を指定する必要があります。  <br/> |[[Tabs] セクション](tabs-section.md) <br/> |
   

