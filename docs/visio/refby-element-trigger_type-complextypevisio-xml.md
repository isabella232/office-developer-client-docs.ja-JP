---
title: RefBy 要素 (Trigger_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: 図面のページへの参照を指定します。
ms.openlocfilehash: e4726a8fe49a7492cd2f7833bbcf5e6810bae18d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572432"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a>RefBy 要素 (Trigger_Type complexType)'Visio XML (')

図面のページへの参照を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> ||
   
## <a name="definition"></a>定義

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Trigger](trigger-elementvisio-xml.md) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。  <br/> |

   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |図面のページの [ID] 属性を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|SV 要素  <br/> |xsd:string  <br/> |必須  <br/> |参照型を指定します。  <br/> |Xsd:string の値を入力します。  <br/> |
   

