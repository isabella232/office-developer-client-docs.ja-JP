---
title: 要素 (Connects_Type の複合型) を接続 ' Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: 線と組織図内のボックスなど、図面内の 2 つの図形間の接続を表します。
ms.openlocfilehash: 1bd3e1f006afe8d5bbb698e0b3a2179b74728315
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805090"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a>要素 (Connects_Type の複合型) を接続 ' Visio XML (')

線と組織図内のボックスなど、図面内の 2 つの図形間の接続を表します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |# .xml のページで、マスターの # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[接続](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |図面内の 2 つの図形間の各接続の**接続**の要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd:string  <br/> |省略可能  <br/> |接続元のセルです。  <br/> |Xsd:string の値を入力します。  <br/> |
|FromPart  <br/> |xsd:int  <br/> |省略可能  <br/> |接続元の図形の一部です。  <br/> |Xsd:int 型の値です。  <br/> |
|FromSheet  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |接続または接続の送信元の図形の ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ToCell  <br/> |xsd:string  <br/> |省略可能  <br/> |接続を作成するセルです。  <br/> |Xsd:string の値を入力します。  <br/> |
|ToPart  <br/> |xsd:int  <br/> |省略可能  <br/> |接続を作成する図形の一部です。  <br/> |Xsd:Int 型の値です。  <br/> |
|ToSheet  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |1 つまたは複数の接続を作成する図形の ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
   

