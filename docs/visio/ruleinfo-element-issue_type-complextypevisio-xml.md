---
title: RuleInfo 要素 (Issue_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: 親の検証の問題に関連する入力規則に関する情報を指定します。
ms.openlocfilehash: ff5a7e4e8918d5ae151a0d4582d1a393509e1b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806314"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a>RuleInfo 要素 (Issue_Type complexType)'Visio XML (')

親の検証の問題に関連する入力規則に関する情報を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[問題](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |文書の 1 つの検証の問題を表します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|規則 Id  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親の問題が関連する入力規則の一意の識別子を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|RuleSetID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親の問題が関連する検証規則のセットの一意の識別子を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
   

