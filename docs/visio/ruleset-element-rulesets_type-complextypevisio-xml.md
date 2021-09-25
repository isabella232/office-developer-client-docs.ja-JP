---
title: RuleSet 要素 (RuleSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: 図の検証ルール セットの 1 つを表します。
ms.openlocfilehash: ab46da07b39a36bc34f21f73e155ac2e62af6d39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598270"
---
# <a name="ruleset-element-rulesets_type-complextype-visio-xml"></a>RuleSet 要素 (RuleSets_Type complexType) (Visio XML)

図の検証ルール セットの 1 つを表します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |ドキュメントの検証ルール セットごとに **RuleSet** 要素が含まれます。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |図の検証ルールセット内の1つの検証ルールを表します。  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |ルールセット プロパティを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|説明  <br/> |xsd:string  <br/> |省略可能  <br/> |検証ルールセットのユーザーインターフェイスに表示される説明を指定します。 既定値は空の文字列です。  <br/> |xsd:string 型の値。  <br/> |
|有効  <br/> |xsd:boolean  <br/> |省略可能  <br/> |現在のドキュメントで検証が実行される時に、指定された検証ルールセットの規則をチェックするかどうかを指定します。 既定値は True です。  <br/> |xsd:boolean 型の値。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |検証ルール セットの一意の識別子を指定します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |検証ルール セットの局所名を指定します。 既定値は NameU 属性値です。  <br/> |xsd:string 型の値。  <br/> |
|NameU  <br/> |xsd:string  <br/> |必須  <br/> |検証ルール セットのユニバーサル名を指定します。  <br/> |xsd:string 型の値。  <br/> |
   

