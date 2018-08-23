---
title: RefBy 要素 (Trigger_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: 図面のページへの参照を指定します。
ms.openlocfilehash: 57ac63c4488b68d3af3c6e4a75417e2c7937723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806160"
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
|[Trigger](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。  <br/> |
|[Trigger](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。  <br/> |
|[Trigger](trigger-elementvisio-xml.md) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |図面のページの [ID] 属性を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|SV 要素  <br/> |xsd:string  <br/> |必須  <br/> |参照型を指定します。  <br/> |Xsd:string の値を入力します。  <br/> |
   

