---
title: スタイル シートの要素 (StyleSheets_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: 図面で定義されているスタイルを表します。
ms.openlocfilehash: 2513c7421dc8f890b7ba63f19cf3d31d23ce65ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806594"
---
# <a name="stylesheet-element-stylesheetstype-complextype-visio-xml"></a>スタイル シートの要素 (StyleSheets_Type complexType)'Visio XML (')

図面で定義されているスタイルを表します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[StyleSheets](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |ドキュメントの**スタイル シート**の要素のコレクションが含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1 つのプロパティを指定します。  <br/> |
|[セクション](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |関連するプロパティのコレクションを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このスタイルを継承する塗りつぶしの書式設定スタイル シートの要素の ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |その親要素内の要素の一意の ID。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |省略可能  <br/> |名前がユーザーによってカスタマイズされているかどうかを示します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |省略可能  <br/> |汎用名がユーザーによってカスタマイズされているかどうかを示します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このスタイルが継承している行の書式設定スタイル シートの要素の ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の名前です。  <br/> |Xsd:string の値を入力します。  <br/> |
|NameU  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の汎用名です。  <br/> |Xsd:string の値を入力します。  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このスタイルを継承するテキストの書式設定スタイル シートの要素の ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
   

