---
title: DataColumn_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344703"
---
# <a name="datacolumntype-complextype-visio-xml"></a>DataColumn_Type complexType (' Visio XML ')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-06-05  <br/> |
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

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|カレンダー  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> ||xsd: _ signedshort 型の値。  <br/> |
|columnnameid  <br/> |xsd: string  <br/> |必須  <br/> ||xsd: string 型の値。  <br/> |
|通貨  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> ||xsd: _ signedshort 型の値。  <br/> |
|DataType  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> ||xsd: _ signedshort 型の値。  <br/> |
|Degree  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> ||xsd:/signedint 型の値。  <br/> |
|displayorder  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> ||xsd:/signedint 型の値。  <br/> |
|displaywidth  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> ||xsd:/signedint 型の値。  <br/> |
|Hyperlink  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||xsd: boolean 型の値。  <br/> |
|Label  <br/> |xsd: string  <br/> |必須  <br/> ||xsd: string 型の値。  <br/> |
|LangID  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> ||xsd:/signedint 型の値。  <br/> |
|変換  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||xsd: boolean 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |必須  <br/> ||xsd: string 型の値。  <br/> |
|OrigLabel  <br/> |xsd: string  <br/> |省略可能  <br/> ||xsd: string 型の値。  <br/> |
|UnitType  <br/> |xsd: string  <br/> |省略可能  <br/> ||xsd: string 型の値。  <br/> |
   

