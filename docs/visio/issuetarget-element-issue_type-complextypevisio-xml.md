---
title: IssueTarget 要素 (Issue_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: 親のターゲットによっては、検証の問題は、ページ、またはページと両方親の検証の問題に関連付けられている図形を指定します。 場合は親の検証の問題の対象は、ドキュメント、ページと図形のどちらも、IssueTarget を指定します。
ms.openlocfilehash: 72789782a37b29daa48cd01adb0b8eda4ebf73ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805650"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a>IssueTarget 要素 (Issue_Type complexType)'Visio XML (')

親のターゲットによっては、検証の問題は、ページ、またはページと両方親の検証の問題に関連付けられている図形を指定します。 場合は親の検証の問題の対象は、ドキュメント、ページと図形のどちらも、 **IssueTarget**を指定します。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
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
|PageID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親の検証の問題に関連付けられているページの一意の識別子を指定します。 ターゲットがドキュメントの場合は、PageID の値は 0 xffffffff にできます。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親の検証の問題に関連付けられている図形の一意の識別子を指定します。 ターゲットが、ドキュメントまたはページの場合は、ShapeID 値 0 xffffffff を使用できます。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
   

