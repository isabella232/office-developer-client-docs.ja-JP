---
title: cp 要素 (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: 対応する Char 要素に従って書式設定された文字プロパティ実行の開始位置を示します。 実行は、テキストの末尾、または次のタグまで定義されます。
ms.openlocfilehash: 1dde00dc4a3f85d0bfc7389f0797dfce33acb444
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586636"
---
# <a name="cp-element-text_type-complextype-visio-xml"></a>cp 要素 (Text_Type complexType) (Visio XML)

対応する Char 要素に従って書式設定された文字プロパティ実行の開始位置を示します。 実行は、テキストの末尾、または次のタグまで定義されます。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[cp_Type](cp_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |図形のテキストが含まれます。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |このプロパティが実行する Char 要素インデックス。  <br/> |xsd:unsignedInt 型の値。  <br/> |
   

