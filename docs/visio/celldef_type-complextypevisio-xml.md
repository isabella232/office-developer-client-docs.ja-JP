---
title: CellDef_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 6471158df8c89e8d7b0202f9bdbce196e24b93b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804977"
---
# <a name="celldeftype-complextype-visio-xml"></a>CellDef_Type complexType'Visio XML (')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**拡張ベース** <br/> |なし  <br/> |
   
## <a name="definition"></a>定義

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
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
|ExternalTaskProject 要素  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
|IX  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||Xsd:unsignedByte の値を入力します。  <br/> |
|N  <br/> |xsd:string  <br/> |必須  <br/> ||Xsd:string の値を入力します。  <br/> |
|S  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||Xsd:unsignedByte の値を入力します。  <br/> |
|SV 要素  <br/> |xsd:token  <br/> |必須  <br/> ||Xsd:token の値を入力します。  <br/> |
   

