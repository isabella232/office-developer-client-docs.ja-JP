---
title: ルールセットの要素 (RuleSets_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: ダイアグラムの検証ルールの 1 つのセットを表します。
ms.openlocfilehash: ae8fc52dd665e51f38c7eeae2f12ff778937d565
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806331"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a>ルールセットの要素 (RuleSets_Type complexType)'Visio XML (')

ダイアグラムの検証ルールの 1 つのセットを表します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[ルールセット](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |各入力規則に違反、文書内の**ルール セット**の要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |図の検証ルール セットに含まれる 1 つの検証ルールを表します。  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |ルール ・ セットのプロパティを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|説明  <br/> |xsd:string  <br/> |省略可能  <br/> |検証ルール セットのユーザー インターフェイスに表示される説明を指定します。 既定値は空の文字列です。  <br/> |Xsd:string の値を入力します。  <br/> |
|Enabled  <br/> |xsd:boolean  <br/> |省略可能  <br/> |現在のドキュメントの検証が発生したときに指定された検証規則セットに規則をチェックするかどうかを指定します。 既定では True です。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |検証ルール セットの一意の識別子を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |ローカル検証ルール セットの名前を指定します。 NameU 属性の値を既定値です。  <br/> |Xsd:string の値を入力します。  <br/> |
|NameU  <br/> |xsd:string  <br/> |必須  <br/> |検証ルール セットの汎用名を指定します。  <br/> |Xsd:string の値を入力します。  <br/> |
   

