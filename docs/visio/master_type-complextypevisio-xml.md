---
title: Master_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 22b619149fc5393f085ca6e245c65ed6058538ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538068"
---
# <a name="mastertype-complextype-visio-xml"></a>Master_Type complexType (Visio XML)

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-06-05  <br/> |
|**拡張ベース** <br/> |None  <br/> |
   
## <a name="definition"></a>定義

```XML
          <xs:complexType name="Master_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="BaseID"
  type="xsd:string"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="MatchByName"
  type="xsd:boolean"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="Hidden"
  type="xsd:boolean"
    />
    <xs:attribute name="IconUpdate"
  type="xsd:boolean"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> ||
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-master_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd: アン Signedshort  <br/> |省略可能  <br/> ||Xsd: _ Signedshort 型の値。  <br/> |
|BaseID  <br/> |xsd: string  <br/> |省略可能  <br/> ||Xsd: string 型の値。  <br/> |
|Hidden  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||Xsd: boolean 型の値。  <br/> |
|IconSize  <br/> |xsd: アン Signedshort  <br/> |省略可能  <br/> ||Xsd: _ Signedshort 型の値。  <br/> |
|IconUpdate  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||Xsd: boolean 型の値。  <br/> |
|ID  <br/> |xsd: アン Signedint  <br/> |必須  <br/> ||Xsd:/Signedint 型の値。  <br/> |
|IsCustomName  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||Xsd: boolean 型の値。  <br/> |
|IsCustomNameU  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||Xsd: boolean 型の値。  <br/> |
|MasterType  <br/> |xsd: アン Signedshort  <br/> |省略可能  <br/> ||Xsd: _ Signedshort 型の値。  <br/> |
|MatchByName  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||Xsd: boolean 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> ||Xsd: string 型の値。  <br/> |
|NameU  <br/> |xsd: string  <br/> |省略可能  <br/> ||Xsd: string 型の値。  <br/> |
|PatternFlags  <br/> |xsd: アン Signedshort  <br/> |省略可能  <br/> ||Xsd: _ Signedshort 型の値。  <br/> |
|プロンプト  <br/> |xsd: string  <br/> |省略可能  <br/> ||Xsd: string 型の値。  <br/> |
|UniqueID  <br/> |xsd: string  <br/> |省略可能  <br/> ||Xsd: string 型の値。  <br/> |
   

