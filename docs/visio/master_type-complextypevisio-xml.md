---
title: Master_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: b4dde4d00552525a5ec17116f96151f39c6d0957
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805820"
---
# <a name="mastertype-complextype-visio-xml"></a>Master_Type complexType'Visio XML (')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**拡張ベース** <br/> |なし  <br/> |
   
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

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> ||
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-master_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> ||Xsd:unsignedShort の値を入力します。  <br/> |
|BaseID  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
|非表示  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||Xsd:boolean の値を入力します。  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> ||Xsd:unsignedShort の値を入力します。  <br/> |
|IconUpdate  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||Xsd:boolean の値を入力します。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> ||Xsd:unsignedInt の値を入力します。  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||Xsd:boolean の値を入力します。  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||Xsd:boolean の値を入力します。  <br/> |
|MasterType  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> ||Xsd:unsignedShort の値を入力します。  <br/> |
|MatchByName  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||Xsd:boolean の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
|NameU  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> ||Xsd:unsignedShort の値を入力します。  <br/> |
|プロンプト  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
   

