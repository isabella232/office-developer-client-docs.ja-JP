---
title: Row 要素 (Controls セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: 図形に定義されている特定のコントロールハンドルのセルを格納します。
ms.openlocfilehash: 0fb31d8066e0a76bfe00735cb5dcc984d02685f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541744"
---
# <a name="row-element-controls-section-visio-xml"></a>Row 要素 (Controls セクション) (Visio XML)

図形に定義されている特定のコントロールハンドルのセルを格納します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |マスター # .xml、ページ # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |図形に定義されている特定のコントロールハンドルのセルを格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |図形に定義されている特定のコントロールハンドルのプロパティが含まれています。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd: boolean  <br/> |省略可能  <br/> |マスターシェイプから継承される行が削除されているかどうかを指定します。  <br/> |Xsd: boolean 型の値。  <br/> |
|IX  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |行の1から始まる識別子を指定します。 これは、同じセクションの他の識別子よりも大きい qiue-v である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、スクラッチ、およびタブセクションにのみ使用されます。 行には、IX 属性または N 属性のいずれかのみを含めることができます。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|LocalName  <br/> |xsd: string  <br/> |省略可能  <br/> |行の一意の言語に依存する名前を指定します。  <br/> |Xsd: string 型の値。  <br/> |
|N  <br/> |xsd: string  <br/> |省略可能  <br/> |一意の言語に依存しない行の名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、および ActionTag セクションにのみ使用されます。 行には、IX 属性または N 属性のいずれかのみを含めることができます。  <br/> |Xsd: string 型の値。  <br/> |
|T  <br/> |xsd: string  <br/> |省略可能  <br/> |Geometry の視覚化で使用される、行で表されるジオメトリックパスの種類を指定します。 T 属性は、[Geometry] セクションにのみ使用されます。  <br/> |Xsd: string 型の値。  <br/> |
   

