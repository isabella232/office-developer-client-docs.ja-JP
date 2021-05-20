---
title: CommentEntry 要素 (CommentList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: 図面内のコメントを識別するために使用するプロパティを指定します。
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540113"
---
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a>CommentEntry 要素 (CommentList_Type complexType) (Visio XML)

図面内のコメントを識別するために使用するプロパティを指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |図面内のコメントを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |作成者を識別する 1 ベースの値。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|CommentID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |図面ページのコメントを識別する一意の値。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|日付  <br/> |xsd:dateTime  <br/> |必須  <br/> |コメントが作成された時間を指定します。  <br/> |xsd:dateTime type 型の値。  <br/> |
|完了  <br/> |xsd:boolean  <br/> |省略可能  <br/> |コメントの現在の状態を指定します。  <br/> |xsd:boolean 型の値。  <br/> |
|EditDate  <br/> |xsd:dateTime  <br/> |省略可能  <br/> |コメントが最後に変更された時間を指定します。  <br/> |xsd:dateTime type 型の値。  <br/> |
|PageID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |コメントが表示されている図面ページを識別する値。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |コメントがオンの図形を識別する値。 ShapeID が指定されていない場合、コメントは図面ページを参照します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
   

