---
title: HeaderFooterFont_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397248"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a>HeaderFooterFont_Type complexType'Visio XML (')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
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

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|文字セット  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||Xsd:unsignedByte の値を入力します。  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||Xsd:unsignedByte の値を入力します。  <br/> |
|文字送り  <br/> |xsd:int  <br/> |省略可能  <br/> ||Xsd:int 型の値です。  <br/> |
|フォント名  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
|Height  <br/> |xsd:int  <br/> |省略可能  <br/> ||Xsd:int 型の値です。  <br/> |
|イタリック  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||Xsd:unsignedByte の値を入力します。  <br/> |
|オリエンテーション  <br/> |xsd:int  <br/> |省略可能  <br/> ||Xsd:int 型の値です。  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||Xsd:unsignedByte の値を入力します。  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||Xsd:unsignedByte の値を入力します。  <br/> |
|品質  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||Xsd:unsignedByte の値を入力します。  <br/> |
|取り消し線  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||Xsd:unsignedByte の値を入力します。  <br/> |
|下線  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> ||Xsd:unsignedByte の値を入力します。  <br/> |
|太さ  <br/> |xsd:int  <br/> |省略可能  <br/> ||Xsd:int 型の値です。  <br/> |
|Width  <br/> |xsd:int  <br/> |省略可能  <br/> ||Xsd:int 型の値です。  <br/> |
   

