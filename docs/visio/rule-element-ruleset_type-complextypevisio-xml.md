---
title: (RuleSet_Type の複合型) のルールの要素 ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: 図の検証ルール セットに含まれる 1 つの検証ルールを表します。
ms.openlocfilehash: feae283c624bdece98dbc1136b0fe8765d911e12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806311"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a>(RuleSet_Type の複合型) のルールの要素 ('Visio XML')

図の検証ルール セットに含まれる 1 つの検証ルールを表します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[ルールセット](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |ダイアグラムの検証ルールの 1 つのセットを表します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |対象オブジェクトに規則を適用するかどうかを決定する論理式を指定します。  <br/> |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |対象のオブジェクトが、検証規則を満たすかどうかを決定する論理式を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|カテゴリ  <br/> |xsd:string  <br/> |省略可能  <br/> |問題ウィンドウの [**カテゴリ**] 列に表示するテキストを指定します。 既定値は空の文字列です。  <br/> |Xsd:string の値を入力します。  <br/> |
|説明  <br/> |xsd:string  <br/> |省略可能  <br/> |ユーザー インターフェイスに表示される入力規則の説明を指定します。 既定では「不明」です。  <br/> |Xsd:string の値を入力します。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |検証ルールの一意の識別子を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|無視  <br/> |xsd:boolean  <br/> |省略可能  <br/> |入力規則が現在無視するかどうかを指定します。 既定では False です。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|NameU  <br/> |xsd:string  <br/> |必須  <br/> |入力規則の汎用名を指定します。  <br/> |Xsd:string の値を入力します。  <br/> |
|RuleTarget  <br/> |xsd:int  <br/> |省略可能  <br/> |検証規則を適用するオブジェクトの種類を指定します。  <br/> |Xsd:int 型の値です。  <br/> |
   

