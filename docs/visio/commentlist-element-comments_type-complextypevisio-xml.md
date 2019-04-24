---
title: コメント list 要素 (Comments_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: 図面内のコメントを指定します。
ms.openlocfilehash: 424eb10ab356fc2b7f07a1fae27a8e2715e3f2fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359431"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a>コメント list 要素 (Comments_Type complexType) (' Visio XML ')

図面内のコメントを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |comments  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[コメント](comments-element-comments_type-complextypevisio-xml.md) <br/> |[Comments_Type](comments_type-complextypevisio-xml.md) <br/> |図面の作成者とコメントを識別するために使用するプロパティを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[コメントエントリ](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |図面内のコメントを識別するために使用するプロパティを指定します。  <br/> |
   
### <a name="attributes"></a>属性

なし。
  

