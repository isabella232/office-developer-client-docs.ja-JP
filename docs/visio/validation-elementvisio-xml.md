---
title: 検証要素 ' Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: 図面に対する図の検証に関する情報を格納します。
ms.openlocfilehash: 7e40cd3a79922b56800cbb566a0d88de23829cc0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382359"
---
# <a name="validation-element-visio-xml"></a>検証要素 ' Visio XML (')

図面に対する図の検証に関する情報を格納します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

なし。
  
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[問題](issues-element-validation_type-complextypevisio-xml.md) <br/> |[Issues_Type](issues_type-complextypevisio-xml.md) <br/> |ドキュメントのすべての**問題**の要素が含まれています。  <br/> |
|[ルールセット](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |各入力規則に違反、文書内の**ルール セット**の要素が含まれています。  <br/> |
|[ValidationProperties](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[ValidationProperties_Type](validationproperties_type-complextypevisio-xml.md) <br/> |ドキュメントの検証に関連するプロパティをカプセル化します。  <br/> |
   
### <a name="attributes"></a>属性

なし。
  

