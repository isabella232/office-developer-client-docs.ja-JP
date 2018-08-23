---
title: RuleSetFlags 要素 (RuleSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c18d3a84-2088-13f7-7b14-1f4c129537b4
description: ルール ・ セットのプロパティを指定します。
ms.openlocfilehash: f656e8ace045d45460ab353444c39c760448aa7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806327"
---
# <a name="rulesetflags-element-rulesettype-complextype-visio-xml"></a>RuleSetFlags 要素 (RuleSet_Type complexType)'Visio XML (')

ルール ・ セットのプロパティを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RuleSetFlags" type="RuleSetFlags_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[ルールセット](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |ダイアグラムの検証ルールの 1 つのセットを表します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|非表示  <br/> |xsd:boolean  <br/> |省略可能  <br/> |チェック] ボックスの一覧を規則でルール セットが表示されるかどうかを指定します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
   

