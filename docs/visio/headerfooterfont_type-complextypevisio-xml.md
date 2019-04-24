---
title: HeaderFooterFont_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335624"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a>HeaderFooterFont_Type complexType (' Visio XML ')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-06-05  <br/> |
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

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd: アン signedbyte  <br/> |省略可能  <br/> ||xsd:/signedbyte 型の値。  <br/> |
|ClipPrecision  <br/> |xsd: アン signedbyte  <br/> |省略可能  <br/> ||xsd:/signedbyte 型の値。  <br/> |
|実際  <br/> |xsd: int  <br/> |省略可能  <br/> ||xsd: int 型の値。  <br/> |
|facename  <br/> |xsd: string  <br/> |省略可能  <br/> ||xsd: string 型の値。  <br/> |
|Height  <br/> |xsd: int  <br/> |省略可能  <br/> ||xsd: int 型の値。  <br/> |
|斜体  <br/> |xsd: アン signedbyte  <br/> |省略可能  <br/> ||xsd:/signedbyte 型の値。  <br/> |
|Orientation  <br/> |xsd: int  <br/> |省略可能  <br/> ||xsd: int 型の値。  <br/> |
|アウト精度  <br/> |xsd: アン signedbyte  <br/> |省略可能  <br/> ||xsd:/signedbyte 型の値。  <br/> |
|PitchAndFamily  <br/> |xsd: アン signedbyte  <br/> |省略可能  <br/> ||xsd:/signedbyte 型の値。  <br/> |
|Quality  <br/> |xsd: アン signedbyte  <br/> |省略可能  <br/> ||xsd:/signedbyte 型の値。  <br/> |
|線  <br/> |xsd: アン signedbyte  <br/> |省略可能  <br/> ||xsd:/signedbyte 型の値。  <br/> |
|Underline  <br/> |xsd: アン signedbyte  <br/> |省略可能  <br/> ||xsd:/signedbyte 型の値。  <br/> |
|太さ  <br/> |xsd: int  <br/> |省略可能  <br/> ||xsd: int 型の値。  <br/> |
|Width  <br/> |xsd: int  <br/> |省略可能  <br/> ||xsd: int 型の値。  <br/> |
   

