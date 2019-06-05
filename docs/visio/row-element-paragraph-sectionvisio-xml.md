---
title: Row 要素 (段落セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 00ecaa82-3b40-24cc-91c0-b2562e92161d
description: 図形のテキストに対する、段落の書式属性を表示します。属性には、インデント、行間隔、箇条書き、および段落の水平方向の配置などがあります。
ms.openlocfilehash: 48d32f3a0712e2ed3110ced545d5b946f147d755
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540820"
---
# <a name="row-element-paragraph-section-visio-xml"></a>Row 要素 (段落セクション) (Visio XML)

図形のテキストに対する、段落の書式属性を表示します。属性には、インデント、行間隔、箇条書き、および段落の水平方向の配置などがあります。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |文書 .xml、master # .xml、ページ # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Row" type="ParagraphRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |図形のテキストに対する、段落の書式属性を表示します。属性には、インデント、行間隔、箇条書き、および段落の水平方向の配置などがあります。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1つのプロパティを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd: boolean  <br/> |省略可能  <br/> |マスターシェイプから継承される行が削除されているかどうかを指定します。  <br/> |Xsd: boolean 型の値。  <br/> |
|IX  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |行の1から始まる識別子を指定します。 これは、同じセクションの他の識別子よりも大きい qiue-v である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、スクラッチ、およびタブセクションにのみ使用されます。 行には、IX 属性または N 属性のいずれかのみを含めることができます。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|LocalName  <br/> |xsd: string  <br/> |省略可能  <br/> |行の一意の言語に依存する名前を指定します。  <br/> |Xsd: string 型の値。  <br/> |
|N  <br/> |xsd: string  <br/> |省略可能  <br/> |一意の言語に依存しない行の名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、および ActionTag セクションにのみ使用されます。 行には、IX 属性または N 属性のいずれかのみを含めることができます。  <br/> |Xsd: string 型の値。  <br/> |
|T  <br/> |xsd: string  <br/> |省略可能  <br/> |Geometry の視覚化で使用される、行で表されるジオメトリックパスの種類を指定します。 T 属性は、[Geometry] セクションにのみ使用されます。  <br/> |Xsd: string 型の値。  <br/> |
   

