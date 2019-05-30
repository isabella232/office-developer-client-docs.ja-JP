---
title: AuthorEntry 要素 (AuthorList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: 図面内のコメントの作成者を識別するために使用するプロパティを指定します。
ms.openlocfilehash: 29dc4459d0df3b914d61140cb2c5f33cc3e1306e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537907"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a>AuthorEntry 要素 (AuthorList_Type complexType) (Visio XML)

図面内のコメントの作成者を識別するために使用するプロパティを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |comments  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |図面の作成者を指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd: アン Signedint  <br/> |必須  <br/> |作成者を識別する1から始まる値。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|イニシャル  <br/> |xsd: string  <br/> |省略可能  <br/> |作成者のイニシャル。  <br/> |Xsd: string 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> |作成者の名前を指定します。  <br/> |Xsd: string 型の値。  <br/> |
|解決 Id  <br/> |xsd: string  <br/> |省略可能  <br/> |作成者の一意の識別子。  <br/> |Xsd: string 型の値。  <br/> |
   

