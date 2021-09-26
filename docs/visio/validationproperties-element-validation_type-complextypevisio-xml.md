---
title: ValidationProperties 要素 (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: ドキュメントの検証に関連するプロパティをカプセル化します。
ms.openlocfilehash: c6608a723a689e958e4a4858753055480fb6d2f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627192"
---
# <a name="validationproperties-element-validation_type-complextype-visio-xml"></a>ValidationProperties 要素 (Validation_Type complexType) (Visio XML)

ドキュメントの検証に関連するプロパティをカプセル化します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[ValidationProperties_Type](validationproperties_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="ValidationProperties" type="ValidationProperties_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Validation](validation-elementvisio-xml.md) <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |図面に対する図の検証に関する情報を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|LastValidated  <br/> |xsd:dateTime  <br/> |必須出席者  <br/> |ドキュメントが最後に検証された日時。  <br/> |xsd:dateTime type 型の値。  <br/> |
|ShowIgnored  <br/> |xsd:boolean  <br/> |必須  <br/> |[問題] ウィンドウに無視された検証の問題を表示するかどうかを指定します。  <br/> |xsd:boolean 型の値。  <br/> |
   

