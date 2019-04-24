---
title: authorentry 要素 (AuthorList_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: 図面内のコメントの作成者を識別するために使用するプロパティを指定します。
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338627"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a>authorentry 要素 (AuthorList_Type complexType) (' Visio XML ')

図面内のコメントの作成者を識別するために使用するプロパティを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[authorlist](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |図面の作成者を指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |作成者を識別する1から始まる値。  <br/> |xsd:/signedint 型の値。  <br/> |
|イニシャル  <br/> |xsd: string  <br/> |省略可能  <br/> |作成者のイニシャル。  <br/> |xsd: string 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> |作成者の名前を指定します。  <br/> |xsd: string 型の値。  <br/> |
|解決 id  <br/> |xsd: string  <br/> |省略可能  <br/> |作成者の一意の識別子。  <br/> |xsd: string 型の値。  <br/> |
   

