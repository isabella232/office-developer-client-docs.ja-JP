---
title: IssueTarget 要素 (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: 親の検証の問題の対象に応じて、親の検証の問題に関連付けられているページ、またはページと図形の両方を指定します。 親の検証の問題の対象がドキュメントの場合は、IssueTarget はページと図形のどちらも指定しません。
ms.openlocfilehash: dd85f62e35d4940da433f365e8c586689315fa9b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574070"
---
# <a name="issuetarget-element-issue_type-complextype-visio-xml"></a>IssueTarget 要素 (Issue_Type complexType) (Visio XML)

親の検証の問題の対象に応じて、親の検証の問題に関連付けられているページ、またはページと図形の両方を指定します。 親の検証の問題の対象がドキュメントの場合は、**IssueTarget** はページと図形のどちらも指定しません。 
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
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
|PageID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親の検証の問題に関連付けられているページの一意の識別子を指定します。 ターゲットがドキュメントの場合は、PageID 値を 0xFFFFFFFF にすることができます。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親の検証の問題に関連付けられている図形の一意の識別子を指定します。 ターゲットがドキュメントまたはページの場合は、ShapeID 値を 0xFFFFFFFF にすることができます。  <br/> |xsd:unsignedInt 型の値。  <br/> |
   

