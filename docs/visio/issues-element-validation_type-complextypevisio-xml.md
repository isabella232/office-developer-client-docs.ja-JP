---
title: "[問題] 要素 (Validation_Type complexType) (' Visio XML ')"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: 文書のすべての Issue 要素を含みます。
ms.openlocfilehash: da3156e34af1536fab39d3d4949acac1efe67264
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339488"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a>[問題] 要素 (Validation_Type complexType) (' Visio XML ')

文書のすべての Issue 要素を含みます。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Issues_Type](issues_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |検証 xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Validation](validation-elementvisio-xml.md) <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |図面に対する図の検証に関する情報を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[問題](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |文書内の1つの検証問題を表します。  <br/> |
   
### <a name="attributes"></a>属性

なし。
  

