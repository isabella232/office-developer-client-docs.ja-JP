---
title: StyleSheet 要素 (StyleSheets_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: 文書内で定義されたスタイルを表します。
ms.openlocfilehash: af1f8270be28e7edabf22d93471517531f5cc226
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329800"
---
# <a name="stylesheet-element-stylesheetstype-complextype-visio-xml"></a>StyleSheet 要素 (StyleSheets_Type complexType) ('Visio XML')

文書内で定義されたスタイルを表します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[StyleSheets](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |ドキュメントの **StyleSheet** 要素のコレクションが含まれます。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1つのプロパティを指定します。  <br/> |
|[セクション](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |関連するプロパティのコレクションを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このスタイルが塗りつぶし書式を継承する StyleSheet 要素の ID です。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親要素内の要素の一意の ID です。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |省略可能  <br/> |ユーザーが名前をカスタマイズしているかどうかを示します。  <br/> |xsd:boolean 型の値。  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |省略可能  <br/> |ユーザーが汎用名をカスタマイズしているかどうかを示します。  <br/> |xsd:boolean 型の値。  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このスタイルが行書式を継承する StyleSheet 要素の ID です。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の名前。  <br/> |xsd:string 型の値。  <br/> |
|NameU  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の汎用名。  <br/> |xsd:string 型の値。  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このスタイルがテキスト形式を継承する StyleSheet 要素の ID です。  <br/> |xsd:unsignedInt 型の値。  <br/> |
   

