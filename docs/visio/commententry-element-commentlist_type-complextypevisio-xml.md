---
title: CommentEntry 要素 (CommentList_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: 図面内のコメントを識別するためのプロパティを指定します。
ms.openlocfilehash: b2ab1925c8b3b9a9c2d67ac48c1db1768f5916b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805043"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a>CommentEntry 要素 (CommentList_Type complexType)'Visio XML (')

図面内のコメントを識別するためのプロパティを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |図面内のコメントを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|著者 Id  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |作成者を識別する 1 から始まる値です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|CommentID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |図面ページにコメントを識別する一意の値です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|日付  <br/> |xsd:dateTime  <br/> |必須  <br/> |コメントが作成された日時を指定します。  <br/> |Xsd:dateTime の値を入力します。  <br/> |
|終了  <br/> |xsd:boolean  <br/> |省略可能  <br/> |コメントの現在の状態を指定します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|EditDate  <br/> |xsd:dateTime  <br/> |省略可能  <br/> |コメントが最後に変更された日時を指定します。  <br/> |Xsd:dateTime の値を入力します。  <br/> |
|PageID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |コメントするには図面のページを識別する値です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |コメントするには図形を識別する値です。 ShapeID が指定されていない場合、コメントは、図面のページを参照します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
   

