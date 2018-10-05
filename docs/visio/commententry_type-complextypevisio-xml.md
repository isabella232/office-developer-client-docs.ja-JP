---
title: CommentEntry_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384795"
---
# <a name="commententrytype-complextype-visio-xml"></a>CommentEntry_Type complexType'Visio XML (')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**拡張ベース** <br/> |xsd:string  <br/> |
   
## <a name="definition"></a>定義

```XML
      <xs:complexType name="CommentEntry_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="AuthorID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Date"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="EditDate"
  type="xsd:dateTime"
    />
    <xs:attribute name="Done"
  type="xsd:boolean"
    />
    <xs:attribute name="CommentID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="AutoCommentType"
  type="xsd:unsignedInt"
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
|著者 Id  <br/> |xsd:unsignedInt  <br/> |必須  <br/> ||Xsd:unsignedInt の値を入力します。  <br/> |
|AutoCommentType  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||Xsd:unsignedInt の値を入力します。  <br/> |
|CommentID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> ||Xsd:unsignedInt の値を入力します。  <br/> |
|日付  <br/> |xsd:dateTime  <br/> |必須  <br/> ||Xsd:dateTime の値を入力します。  <br/> |
|終了  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||Xsd:boolean の値を入力します。  <br/> |
|EditDate  <br/> |xsd:dateTime  <br/> |省略可能  <br/> ||Xsd:dateTime の値を入力します。  <br/> |
|PageID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> ||Xsd:unsignedInt の値を入力します。  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||Xsd:unsignedInt の値を入力します。  <br/> |
   

