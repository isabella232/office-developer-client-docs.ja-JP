---
title: authorlist 要素 (Comments_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: 図面内のコメントの作成者を指定します。
ms.openlocfilehash: af1b1889fa3736931c9abde35191cf5cb3e1bbd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338417"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a>authorlist 要素 (Comments_Type complexType) (' Visio XML ')

図面内のコメントの作成者を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |comments  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[コメント](comments-element-comments_type-complextypevisio-xml.md) <br/> |[Comments_Type](comments_type-complextypevisio-xml.md) <br/> |図面内のコメントを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[authorentry](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |図面内のコメントの作成者を識別するプロパティを指定します。  <br/> |
   
### <a name="attributes"></a>属性

なし。
  

