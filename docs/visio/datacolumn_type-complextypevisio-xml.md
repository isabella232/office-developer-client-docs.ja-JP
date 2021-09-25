---
title: DataColumn_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: a925d01365d78c899c5cd828c604a6ee18b0242b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582842"
---
# <a name="datacolumn_type-complextype-visio-xml"></a>DataColumn_Type complexType (Visio XML)

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**拡張ベース** <br/> |なし  <br/> |
   
## <a name="definition"></a>定義

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|予定表  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> ||xsd:unsignedShort 型の値。  <br/> |
|ColumnNameID  <br/> |xsd:string  <br/> |必須  <br/> ||xsd:string 型の値。  <br/> |
|通貨  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> ||xsd:unsignedShort 型の値。  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> ||xsd:unsignedShort 型の値。  <br/> |
|Degree  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||xsd:unsignedInt 型の値。  <br/> |
|DisplayOrder  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||xsd:unsignedInt 型の値。  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||xsd:unsignedInt 型の値。  <br/> |
|ハイパーリンク  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||xsd:boolean 型の値。  <br/> |
|ラベル  <br/> |xsd:string  <br/> |必須  <br/> ||xsd:string 型の値。  <br/> |
|LangID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||xsd:unsignedInt 型の値。  <br/> |
|マッピングされた  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||xsd:boolean 型の値。  <br/> |
|名前  <br/> |xsd:string  <br/> |必須  <br/> ||xsd:string 型の値。  <br/> |
|OrigLabel  <br/> |xsd:string  <br/> |省略可能  <br/> ||xsd:string 型の値。  <br/> |
|UnitType  <br/> |xsd:string  <br/> |省略可能  <br/> ||xsd:string 型の値。  <br/> |
   

