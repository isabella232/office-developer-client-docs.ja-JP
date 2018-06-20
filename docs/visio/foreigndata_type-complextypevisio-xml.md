---
title: ForeignData_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 1d9358de2f88a1b9e035ecf4966544ea935f8b2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805442"
---
# <a name="foreigndatatype-complextype-visio-xml"></a>ForeignData_Type complexType'Visio XML (')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**拡張機能の基本** <br/> |なし  <br/> |
   
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

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |省略可能  <br/> ||Xsd:double 型の値です。  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |省略可能  <br/> ||Xsd:token の値を入力します。  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |省略可能  <br/> ||Xsd:double 型の値です。  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |省略可能  <br/> ||Xsd:double 型の値です。  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |必須  <br/> ||Xsd:token の値を入力します。  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> ||Xsd:unsignedShort の値を入力します。  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |省略可能  <br/> ||Xsd:double 型の値です。  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||Xsd:unsignedInt の値を入力します。  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |省略可能  <br/> ||Xsd:double 型の値です。  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||Xsd:boolean の値を入力します。  <br/> |
   

