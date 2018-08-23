---
title: コメント要素 (Comments_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: 図面内のコメント、作成者を識別するためのプロパティを指定します。
ms.openlocfilehash: 77695fb32aa88cb6c2b6ac5e9bff99fa12e262bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805044"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a>コメント要素 (Comments_Type complexType)'Visio XML (')

図面内のコメント、作成者を識別するためのプロパティを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Comments_Type](comments_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

なし。
  
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |図面の作成者を指定します。  <br/> |
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |図面内のコメントを指定します。  <br/> |
   
### <a name="attributes"></a>属性

なし。
  

