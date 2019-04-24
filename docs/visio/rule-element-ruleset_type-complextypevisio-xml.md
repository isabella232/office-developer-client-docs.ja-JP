---
title: Rule 要素 (RuleSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: 図の検証ルール セットに含まれる 1 つの検証ルールを表します。
ms.openlocfilehash: 92d52456164b89ff2aad31fa8d8f02f818c8bd1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358801"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a>Rule 要素 (RuleSet_Type complexType) (' Visio XML ')

図の検証ルール セットに含まれる 1 つの検証ルールを表します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |検証 xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[RuleSet](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |1組のダイアグラム検証ルールを表します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[rulefilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |ターゲットオブジェクトに検証ルールを適用する必要があるかどうかを決定する論理式を指定します。  <br/> |
|[ルール](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |ターゲットオブジェクトが検証規則を満たしているかどうかを決定する論理式を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|カテゴリ  <br/> |xsd: string  <br/> |省略可能  <br/> |[問題] ウィンドウの [**カテゴリ**] 列に表示されるテキストを指定します。 既定値は空の文字列です。  <br/> |xsd: string 型の値。  <br/> |
|説明  <br/> |xsd: string  <br/> |省略可能  <br/> |ユーザーインターフェイスに表示される入力規則の説明を指定します。 既定値は "Unknown" です。  <br/> |xsd: string 型の値。  <br/> |
|ID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |入力規則の一意の識別子を指定します。  <br/> |xsd:/signedint 型の値。  <br/> |
|Ignored  <br/> |xsd: boolean  <br/> |省略可能  <br/> |検証ルールが現在無視されているかどうかを指定します。 既定値は False です。  <br/> |xsd: boolean 型の値。  <br/> |
|NameU  <br/> |xsd: string  <br/> |必須  <br/> |入力規則の汎用名を指定します。  <br/> |xsd: string 型の値。  <br/> |
|ruletarget  <br/> |xsd: int  <br/> |省略可能  <br/> |入力規則を適用するオブジェクトの種類を指定します。  <br/> |xsd: int 型の値。  <br/> |
   

