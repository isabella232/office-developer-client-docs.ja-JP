---
title: DocumentSheet_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 47378b039d11294dcb566f61cf20b0ed1ed7fed8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805263"
---
# <a name="documentsheettype-complextype-visio-xml"></a>DocumentSheet_Type complexType'Visio XML (')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**拡張ベース** <br/> |Sheet_Type  <br/> |
   
## <a name="definition"></a>定義

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
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
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||Xsd:boolean の値を入力します。  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||Xsd:boolean の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
|NameU  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
   

