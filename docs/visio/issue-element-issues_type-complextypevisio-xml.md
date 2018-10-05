---
title: 問題の要素 (Issues_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: 文書の 1 つの検証の問題を表します。
ms.openlocfilehash: 4ebe7d2d8b2b4627fb9c9e12113ef23ce19db52e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389842"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a>問題の要素 (Issues_Type complexType)'Visio XML (')

文書の 1 つの検証の問題を表します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[問題](issues-element-validation_type-complextypevisio-xml.md) <br/> |[Issues_Type](issues_type-complextypevisio-xml.md) <br/> |ドキュメントのすべての**問題**の要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[IssueTarget](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |親のターゲットによっては、検証の問題は、ページ、またはページと両方親の検証の問題に関連付けられている図形を指定します。  <br/> |
|[RuleInfo](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |親の検証の問題に関連する入力規則に関する情報を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |検証の問題の一意の識別子を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|無視  <br/> |xsd:boolean  <br/> |省略可能  <br/> |親の検証の問題に関連する入力規則に関する情報を指定します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
   

