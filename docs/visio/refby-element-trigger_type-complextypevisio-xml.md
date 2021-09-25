---
title: RefBy 要素 (Trigger_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: 図面内のページへの参照を指定します。
ms.openlocfilehash: 4b38c508b2c6d417ffbddbf1cfed9945050ce670
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565906"
---
# <a name="refby-element-trigger_type-complextype-visio-xml"></a>RefBy 要素 (Trigger_Type complexType) (Visio XML)

図面内のページへの参照を指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**名詞空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> ||
   
## <a name="definition"></a>定義

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Trigger](trigger-elementvisio-xml.md) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Microsoft Visioに、Visio ファイル内のドキュメント パーツ間のリレーションシップを再計算するVisioします。  <br/> |

   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |図面内のページの ID 属性を指定します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|T  <br/> |xsd:string  <br/> |必須  <br/> |参照の種類を指定します。  <br/> |xsd:string 型の値。  <br/> |
   

