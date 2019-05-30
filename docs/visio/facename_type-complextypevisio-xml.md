---
title: FaceName_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: f0a136cec6d620ba7001ed0e6fae01af82c2180d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542899"
---
# <a name="facenametype-complextype-visio-xml"></a>FaceName_Type complexType (Visio XML)

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-06-05  <br/> |
|**拡張ベース** <br/> |None  <br/> |
   
## <a name="definition"></a>定義

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
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
|CharSets  <br/> |xsd: string  <br/> |省略可能  <br/> ||Xsd: string 型の値。  <br/> |
|フラグ  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> ||Xsd:/Signedint 型の値。  <br/> |
|NameU  <br/> |xsd: string  <br/> |必須  <br/> ||Xsd: string 型の値。  <br/> |
|Panos  <br/> |xsd: string  <br/> |省略可能  <br/> ||Xsd: string 型の値。  <br/> |
|Panose  <br/> |xsd: string  <br/> |省略可能  <br/> ||Xsd: string 型の値。  <br/> |
|UnicodeRanges  <br/> |xsd: string  <br/> |省略可能  <br/> ||Xsd: string 型の値。  <br/> |
   

