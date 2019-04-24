---
title: CommentEntry_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334945"
---
# <a name="commententrytype-complextype-visio-xml"></a>CommentEntry_Type complexType (' Visio XML ')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-06-05  <br/> |
|**拡張ベース** <br/> |xsd: string  <br/> |
   
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

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd: アン signedint  <br/> |必須  <br/> ||xsd:/signedint 型の値。  <br/> |
|autoコメントの種類  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> ||xsd:/signedint 型の値。  <br/> |
|CommentID  <br/> |xsd: アン signedint  <br/> |必須  <br/> ||xsd:/signedint 型の値。  <br/> |
|日付  <br/> |xsd: dateTime  <br/> |必須  <br/> ||xsd: dateTime 型の値。  <br/> |
|完了  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||xsd: boolean 型の値。  <br/> |
|EditDate  <br/> |xsd: dateTime  <br/> |省略可能  <br/> ||xsd: dateTime 型の値。  <br/> |
|PageID  <br/> |xsd: アン signedint  <br/> |必須  <br/> ||xsd:/signedint 型の値。  <br/> |
|ShapeID  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> ||xsd:/signedint 型の値。  <br/> |
   

