---
title: /出力先要素 (Issue_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: 親の検証問題のターゲットに応じて、親の検証の問題に関連付けられているページまたはページと図形の両方を指定します。 親の検証問題のターゲットがドキュメントの場合は、ページまたは図形のどちらも対象外になります。
ms.openlocfilehash: 74005bfb6035e32b7b34fdd5a8a5737813a562a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332523"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a>/出力先要素 (Issue_Type complexType) (' Visio XML ')

親の検証問題のターゲットに応じて、親の検証の問題に関連付けられているページまたはページと図形の両方を指定します。 親の検証問題のターゲットがドキュメントの場合は、ページまたは図形のどちらも**対象**外になります。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |検証 xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[問題](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |文書内の1つの検証問題を表します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |親の検証問題に関連付けられているページの一意の識別子を指定します。 ターゲットがドキュメントの場合、PageID の値は0xffffffff になります。  <br/> |xsd:/signedint 型の値。  <br/> |
|ShapeID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |親の検証問題に関連付けられている図形の一意の識別子を指定します。 ターゲットがドキュメントまたはページである場合、ShapeID の値は0xffffffff にすることができます。  <br/> |xsd:/signedint 型の値。  <br/> |
   

