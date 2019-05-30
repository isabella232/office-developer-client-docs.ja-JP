---
title: ForeignData_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 39396ef0db5b78d6f32d8828103eecd105f8b91d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539864"
---
# <a name="foreigndatatype-complextype-visio-xml"></a>ForeignData_Type complexType (Visio XML)

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-06-05  <br/> |
|**拡張ベース** <br/> |None  <br/> |
   
## <a name="definition"></a>定義

```XML
          <xs:complexType name="ForeignData_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ForeignType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="ObjectType"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ShowAsIcon"
  type="xsd:boolean"
    />
    <xs:attribute name="ObjectWidth"
  type="xsd:double"
    />
    <xs:attribute name="ObjectHeight"
  type="xsd:double"
    />
    <xs:attribute name="MappingMode"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ExtentX"
  type="xsd:double"
    />
    <xs:attribute name="ExtentY"
  type="xsd:double"
    />
    <xs:attribute name="CompressionType"
  type="xsd:token"
    />
    <xs:attribute name="CompressionLevel"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd: double  <br/> |省略可能  <br/> ||Xsd: double 型の値。  <br/> |
|CompressionType  <br/> |xsd: token  <br/> |省略可能  <br/> ||Xsd: token 型の値。  <br/> |
|ExtentX  <br/> |xsd: double  <br/> |省略可能  <br/> ||Xsd: double 型の値。  <br/> |
|ExtentY  <br/> |xsd: double  <br/> |省略可能  <br/> ||Xsd: double 型の値。  <br/> |
|ForeignType  <br/> |xsd: token  <br/> |必須  <br/> ||Xsd: token 型の値。  <br/> |
|MappingMode  <br/> |xsd: アン Signedshort  <br/> |省略可能  <br/> ||Xsd: _ Signedshort 型の値。  <br/> |
|ObjectHeight  <br/> |xsd: double  <br/> |省略可能  <br/> ||Xsd: double 型の値。  <br/> |
|ObjectType  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> ||Xsd:/Signedint 型の値。  <br/> |
|ObjectWidth  <br/> |xsd: double  <br/> |省略可能  <br/> ||Xsd: double 型の値。  <br/> |
|ShowAsIcon  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||Xsd: boolean 型の値。  <br/> |
   

