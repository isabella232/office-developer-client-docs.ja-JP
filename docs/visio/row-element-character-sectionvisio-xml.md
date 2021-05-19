---
title: Row 要素 (Character Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 764a8e77-5308-e6ce-8763-dc6e6090da9d
description: 図形のテキスト実行の書式設定属性 (フォント、色、テキスト スタイル、大文字と小文字、基準線を基準にした位置、ポイント サイズなど) を表示します。
ms.openlocfilehash: afff4dcb809bf73da6ada25045678711ade75b6b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541786"
---
# <a name="row-element-character-section-visio-xml"></a>Row 要素 (Character Section) (Visio XML)

図形のテキスト実行の書式設定属性 (フォント、色、テキスト スタイル、大文字と小文字、基準線を基準にした位置、ポイント サイズなど) を表示します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |document.xml、master#.xml、page#.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Row" type="CharacterRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |図形のテキスト実行の書式設定属性 (フォント、色、テキスト スタイル、大文字と小文字、基準線を基準にした位置、ポイント サイズなど) を表示します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1 つのプロパティを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |省略可能  <br/> |それ以外の場合はマスター図形から継承される行が削除されたかどうかを指定します。  <br/> |xsd:boolean 型の値。  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |行の 1 ベースの識別子を指定します。 これは、同じセクション内の他の識別子よりも長く、unqiue である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、Scratch、および Tabs セクションでのみ使用されます。 行には IX 属性または N 属性のいずれかを指定できます。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|LocalName  <br/> |xsd:string  <br/> |省略可能  <br/> |行の一意の言語依存の名前を指定します。  <br/> |xsd:string 型の値。  <br/> |
|N  <br/> |xsd:string  <br/> |省略可能  <br/> |行の一意の言語に依存しない名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、ActionTag セクションにのみ使用されます。 行には IX 属性または N 属性のいずれかを指定できます。  <br/> |xsd:string 型の値。  <br/> |
|T  <br/> |xsd:string  <br/> |省略可能  <br/> |行で表され、ジオメトリの視覚化で使用されるジオメトリ パスの種類を指定します。 T 属性は、[Geometry] セクションにのみ使用されます。  <br/> |xsd:string 型の値。  <br/> |
   

