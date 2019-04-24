---
title: ルールセット要素 (RuleSets_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: 1組のダイアグラム検証ルールを表します。
ms.openlocfilehash: 1231e8cdb3c8781dc47f470c0477b4585b1331c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318915"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a>ルールセット要素 (RuleSets_Type complexType) (' Visio XML ')

1組のダイアグラム検証ルールを表します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |検証 xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |文書内**** の各入力規則のルールセット要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |図の検証ルール セットに含まれる 1 つの検証ルールを表します。  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |ルールセットのプロパティを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|説明  <br/> |xsd: string  <br/> |省略可能  <br/> |入力規則セットのユーザーインターフェイスに表示される説明を指定します。 既定値は空の文字列です。  <br/> |xsd: string 型の値。  <br/> |
|有効  <br/> |xsd: boolean  <br/> |省略可能  <br/> |現在の文書に対して検証がトリガーされたときに、指定した入力規則セットの規則をチェックするかどうかを指定します。 既定値は True です。  <br/> |xsd: boolean 型の値。  <br/> |
|ID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |入力規則セットの一意の識別子を指定します。  <br/> |xsd:/signedint 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> |入力規則セットのローカル名を指定します。 既定値は NameU attribute 値です。  <br/> |xsd: string 型の値。  <br/> |
|NameU  <br/> |xsd: string  <br/> |必須  <br/> |入力規則セットの汎用名を指定します。  <br/> |xsd: string 型の値。  <br/> |
   

