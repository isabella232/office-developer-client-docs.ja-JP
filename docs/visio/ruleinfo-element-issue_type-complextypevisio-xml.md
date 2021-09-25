---
title: RuleInfo 要素 (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: 親検証の問題に関連する検証ルールに関する情報を指定します。
ms.openlocfilehash: 367c678d14531bd9e9d5dc86956aeb0ff42757fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623020"
---
# <a name="ruleinfo-element-issue_type-complextype-visio-xml"></a>RuleInfo 要素 (Issue_Type complexType) (Visio XML)

親検証の問題に関連する検証ルールに関する情報を指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Issue](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |文書内の1つの検証問題を表します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|RuleID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親の問題に関連する検証ルールの一意の識別子を指定します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|RuleSetID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親の問題に関連する検証ルール セットの一意の識別子を指定します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
   

