---
title: Validation 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: 図面に対する図の検証に関する情報を格納します。
ms.openlocfilehash: c17cd06a602ccf4e9ae93cb4babd12b0a584d0a1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597752"
---
# <a name="validation-element-visio-xml"></a>Validation 要素 (Visio XML)

図面に対する図の検証に関する情報を格納します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

なし。
  
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Issues](issues-element-validation_type-complextypevisio-xml.md) <br/> |[Issues_Type](issues_type-complextypevisio-xml.md) <br/> |ドキュメントのすべての **Issue** 要素が含まれます。  <br/> |
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |ドキュメントの検証ルール セットごとに **RuleSet** 要素が含まれます。  <br/> |
|[ValidationProperties](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[ValidationProperties_Type](validationproperties_type-complextypevisio-xml.md) <br/> |ドキュメントの検証に関連するプロパティをカプセル化します。  <br/> |
   
### <a name="attributes"></a>属性

なし。
  

