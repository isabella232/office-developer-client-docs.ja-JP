---
title: AuthorEntry 要素 (AuthorList_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: 図面内のコメントの作成者を識別するためのプロパティを指定します。
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386333"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a>AuthorEntry 要素 (AuthorList_Type complexType)'Visio XML (')

図面内のコメントの作成者を識別するためのプロパティを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |図面の作成者を指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |作成者を識別する 1 から始まる値です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|Initials  <br/> |xsd:string  <br/> |省略可能  <br/> |作成者のイニシャルです。  <br/> |Xsd:string の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |作成者の名前。  <br/> |Xsd:string の値を入力します。  <br/> |
|ResolutionID  <br/> |xsd:string  <br/> |省略可能  <br/> |作成者の一意の識別子です。  <br/> |Xsd:string の値を入力します。  <br/> |
   

