---
title: コメント entry 要素 (CommentList_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: 図面内のコメントを識別するために使用するプロパティを指定します。
ms.openlocfilehash: 79d15b95f986826a4848c2dfbb003255d3482134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329541"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a>コメント entry 要素 (CommentList_Type complexType) (' Visio XML ')

図面内のコメントを識別するために使用するプロパティを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |comments  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |図面内のコメントを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |作成者を識別する1から始まる値。  <br/> |xsd:/signedint 型の値。  <br/> |
|CommentID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |図面ページのコメントを識別する一意の値。  <br/> |xsd:/signedint 型の値。  <br/> |
|日付  <br/> |xsd: dateTime  <br/> |必須  <br/> |コメントが作成された日時を指定します。  <br/> |xsd: dateTime 型の値。  <br/> |
|完了  <br/> |xsd: boolean  <br/> |省略可能  <br/> |コメントの現在の状態を指定します。  <br/> |xsd: boolean 型の値。  <br/> |
|EditDate  <br/> |xsd: dateTime  <br/> |省略可能  <br/> |コメントが最後に変更された日時を指定します。  <br/> |xsd: dateTime 型の値。  <br/> |
|PageID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |コメントがある図面ページを識別する値。  <br/> |xsd:/signedint 型の値。  <br/> |
|ShapeID  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |コメントがある図形を識別する値。 ShapeID が指定されていない場合、コメントは図面ページを参照します。  <br/> |xsd:/signedint 型の値。  <br/> |
   

