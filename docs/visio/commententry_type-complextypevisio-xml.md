---
title: CommentEntry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 840f660d72acbda052d4729846d8a26686d82b2a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540127"
---
# <a name="commententry_type-complextype-visio-xml"></a>CommentEntry_Type complexType (Visio XML)

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
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

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> ||xsd:unsignedInt 型の値。  <br/> |
|AutoCommentType  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||xsd:unsignedInt 型の値。  <br/> |
|CommentID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> ||xsd:unsignedInt 型の値。  <br/> |
|日付  <br/> |xsd:dateTime  <br/> |必須  <br/> ||xsd:dateTime type 型の値。  <br/> |
|完了  <br/> |xsd:boolean  <br/> |省略可能  <br/> ||xsd:boolean 型の値。  <br/> |
|EditDate  <br/> |xsd:dateTime  <br/> |省略可能  <br/> ||xsd:dateTime type 型の値。  <br/> |
|PageID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> ||xsd:unsignedInt 型の値。  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> ||xsd:unsignedInt 型の値。  <br/> |
   

