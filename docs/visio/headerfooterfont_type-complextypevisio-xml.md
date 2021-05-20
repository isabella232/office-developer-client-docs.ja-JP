---
title: HeaderFooterFont_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: dd99d87e0d80aad3bcde31e4834337ee59088da2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541072"
---
# <a name="headerfooterfont_type-complextype-visio-xml"></a>HeaderFooterFont_Type complexType (Visio XML)

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**拡張ベース** <br/> |なし  <br/> |
   
## <a name="definition"></a>定義

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
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
|CharSet  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||xsd:unsignedByte 型の値。  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||xsd:unsignedByte 型の値。  <br/> |
|Escapement  <br/> |xsd:int  <br/> |省略可能  <br/> ||xsd:int 型の値。  <br/> |
|FaceName  <br/> |xsd:string  <br/> |省略可能  <br/> ||xsd:string 型の値。  <br/> |
|Height  <br/> |xsd:int  <br/> |省略可能  <br/> ||xsd:int 型の値。  <br/> |
|斜体  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||xsd:unsignedByte 型の値。  <br/> |
|Orientation  <br/> |xsd:int  <br/> |省略可能  <br/> ||xsd:int 型の値。  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||xsd:unsignedByte 型の値。  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||xsd:unsignedByte 型の値。  <br/> |
|品質  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||xsd:unsignedByte 型の値。  <br/> |
|StrikeOut  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||xsd:unsignedByte 型の値。  <br/> |
|下線  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||xsd:unsignedByte 型の値。  <br/> |
|太さ  <br/> |xsd:int  <br/> |省略可能  <br/> ||xsd:int 型の値。  <br/> |
|Width  <br/> |xsd:int  <br/> |省略可能  <br/> ||xsd:int 型の値。  <br/> |
   

