---
title: MasterShortcut_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: 23d5de92be151b9ab6819296456746087573e7c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341693"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a>MasterShortcut_Type complexType (' Visio XML ')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-06-05  <br/> |
|**拡張ベース** <br/> |なし  <br/> |
   
## <a name="definition"></a>定義

```XML
          <xs:complexType name="MasterShortcut_Type">
          
          <xs:all>
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
    <xs:attribute name="ShortcutURL"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutHelp"
  type="xsd:string"
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
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> ||xsd: _ signedshort 型の値。  <br/> |
|IconSize  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> ||xsd: _ signedshort 型の値。  <br/> |
|ID  <br/> |xsd: アン signedint  <br/> |必須  <br/> ||xsd:/signedint 型の値。  <br/> |
|iscustomname  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||xsd: boolean 型の値。  <br/> |
|IsCustomNameU  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||xsd: boolean 型の値。  <br/> |
|MasterType  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> ||xsd: _ signedshort 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> ||xsd: string 型の値。  <br/> |
|NameU  <br/> |xsd: string  <br/> |省略可能  <br/> ||xsd: string 型の値。  <br/> |
|PatternFlags  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> ||xsd: _ signedshort 型の値。  <br/> |
|プロンプト  <br/> |xsd: string  <br/> |省略可能  <br/> ||xsd: string 型の値。  <br/> |
|ShortcutHelp  <br/> |xsd: string  <br/> |省略可能  <br/> ||xsd: string 型の値。  <br/> |
|ShortcutURL  <br/> |xsd: string  <br/> |省略可能  <br/> ||xsd: string 型の値。  <br/> |
   

