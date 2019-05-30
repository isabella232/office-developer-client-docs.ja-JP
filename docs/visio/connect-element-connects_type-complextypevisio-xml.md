---
title: Connect 要素 (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: 組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。
ms.openlocfilehash: 3450a07e042fc633b9cd4952d9b3ad6b8190ed1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541996"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a>Connect 要素 (Connects_Type complexType) (Visio XML)

組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |ページ # .xml、マスター # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |図面内の2つの図形を接続するための**Connect**要素を含みます。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd: string  <br/> |省略可能  <br/> |接続元のセルを指定します。  <br/> |Xsd: string 型の値。  <br/> |
|FromPart  <br/> |xsd: int  <br/> |省略可能  <br/> |接続元の図形の部分を指定します。  <br/> |Xsd: int 型の値。  <br/> |
|FromSheet  <br/> |xsd: アン Signedint  <br/> |必須  <br/> |1つまたは複数の接続を開始する図形の ID を指定します。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|ToCell  <br/> |xsd: string  <br/> |省略可能  <br/> |接続を確立するセルを指定します。  <br/> |Xsd: string 型の値。  <br/> |
|ToPart  <br/> |xsd: int  <br/> |省略可能  <br/> |図形の接続先となる部分を指定します。  <br/> |Xsd: Int 型の値。  <br/> |
|ToSheet  <br/> |xsd: アン Signedint  <br/> |必須  <br/> |1つまたは複数の接続を確立する図形の ID を指定します。  <br/> |Xsd:/Signedint 型の値。  <br/> |
   

