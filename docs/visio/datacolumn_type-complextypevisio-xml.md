---
title: DataColumn_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 9d334190b686f3b2c5e25a31336c668c957e820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805156"
---
# <a name="datacolumntype-complextype-visio-xml"></a>DataColumn_Type complexType'Visio XML (')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
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

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|予定表  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> ||Xsd:unsignedShort の値を入力します。  <br/> |
|ColumnNameID  <br/> |xsd:string  <br/> |必須  <br/> ||Xsd:string の値を入力します。  <br/> |
|通貨型 (Currency)  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> ||Xsd:unsignedShort の値を入力します。  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> ||Xsd:unsignedShort の値を入力します。  <br/> |
|Degree  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||Xsd:unsignedInt の値を入力します。  <br/> |
|DisplayOrder  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||Xsd:unsignedInt の値を入力します。  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||Xsd:unsignedInt の値を入力します。  <br/> |
|Hyperlink  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||Xsd:boolean の値を入力します。  <br/> |
|ラベル  <br/> |xsd:string  <br/> |必須  <br/> ||Xsd:string の値を入力します。  <br/> |
|LangID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||Xsd:unsignedInt の値を入力します。  <br/> |
|マップ  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||Xsd:boolean の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |必須  <br/> ||Xsd:string の値を入力します。  <br/> |
|OrigLabel  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
|UnitType  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
   

