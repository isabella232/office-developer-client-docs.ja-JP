---
title: HeaderFooter_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5fcf3d9-c11a-ed5e-0bf5-e706259ef30b
ms.openlocfilehash: 581101909096d4ee8a4f44c8e9e95dab0313ed7c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384508"
---
# <a name="headerfootertype-complextype-visio-xml"></a>HeaderFooter_Type complexType'Visio XML (')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**拡張ベース** <br/> |なし  <br/> |
   
## <a name="definition"></a>定義

```XML
          <xs:complexType name="HeaderFooter_Type">
          
          <xs:all>
    <xs:element name="HeaderMargin"  type="HeaderMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterMargin"  type="FooterMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderLeft"  type="HeaderLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderCenter"  type="HeaderCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderRight"  type="HeaderRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterLeft"  type="FooterLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterCenter"  type="FooterCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterRight"  type="FooterRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderFooterFont"  type="HeaderFooterFont_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="HeaderFooterColor"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[FooterCenter](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterCenter_Type](footercenter_type-complextypevisio-xml.md) <br/> ||
|[FooterLeft](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterLeft_Type](footerleft_type-complextypevisio-xml.md) <br/> ||
|[FooterMargin](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterMargin_Type](footermargin_type-complextypevisio-xml.md) <br/> ||
|[FooterRight](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterRight_Type](footerright_type-complextypevisio-xml.md) <br/> ||
|[HeaderCenter](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderCenter_Type](headercenter_type-complextypevisio-xml.md) <br/> ||
|[HeaderFooterFont](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> ||
|[HeaderLeft](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderLeft_Type](headerleft_type-complextypevisio-xml.md) <br/> ||
|[HeaderMargin](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderMargin_Type](headermargin_type-complextypevisio-xml.md) <br/> ||
|[HeaderRight](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderRight_Type](headerright_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|HeaderFooterColor  <br/> |xsd:string  <br/> |省略可能  <br/> ||Xsd:string の値を入力します。  <br/> |
   

