---
title: EventItem_Type complexType (xml Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: d294e826b90fe490bdf68cb12fae86e8f676aec6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582744"
---
# <a name="eventitem_type-complextype-visio-xml"></a>EventItem_Type complexType (xml Visio)

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**拡張ベース** <br/> |なし  <br/> |
   
## <a name="definition"></a>定義

```XML
      <xs:complexType name="EventItem_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Action"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="EventCode"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
    <xs:attribute name="Target"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="TargetArgs"
  type="xsd:string"
     use="required"
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
|アクション  <br/> |xsd:unsignedShort  <br/> |必須  <br/> ||xsd:unsignedShort 型の値。  <br/> |
|有効  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||xsd:boolean 型の値。  <br/> |
|EventCode  <br/> |xsd:unsignedShort  <br/> |必須出席者  <br/> ||xsd:unsignedShort 型の値。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> ||xsd:unsignedInt 型の値。  <br/> |
|Target  <br/> |xsd:string  <br/> |必須  <br/> ||xsd:string 型の値。  <br/> |
|TargetArgs  <br/> |xsd:string  <br/> |必須  <br/> ||xsd:string 型の値。  <br/> |
   

