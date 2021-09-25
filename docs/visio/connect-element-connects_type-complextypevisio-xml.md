---
title: Connect要素 (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: 組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。
ms.openlocfilehash: 933a58a4afece3798e419f1a483b00f0d823961a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560012"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a>Connect要素 (Connects_Type complexType) (Visio XML)

組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |図面内の **2 Connect** 間の接続ごとに 1 つの要素を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd:string  <br/> |省略可能  <br/> |接続の開始元のセル。  <br/> |xsd:string 型の値。  <br/> |
|FromPart  <br/> |xsd:int  <br/> |省略可能  <br/> |接続の発生元となる図形の部分。  <br/> |xsd:int 型の値。  <br/> |
|FromSheet  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |接続または接続の発生元となる図形の ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ToCell  <br/> |xsd:string  <br/> |省略可能  <br/> |接続が行われたセル。  <br/> |xsd:string 型の値。  <br/> |
|ToPart  <br/> |xsd:int  <br/> |省略可能  <br/> |接続が行われた図形の部分。  <br/> |xsd:Int 型の値。  <br/> |
|ToSheet  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |1 つ以上の接続が作成される図形の ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
   

