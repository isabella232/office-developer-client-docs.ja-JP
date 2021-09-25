---
title: Shape 要素 (Shapes_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Master、Page、またはグループ図形要素で図形を定義する要素を含む。
ms.openlocfilehash: 6c0d414fb3794ff1e377e908de38c694c9f1babd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622936"
---
# <a name="shape-element-shapes_type-complextype-visio-xml"></a>Shape 要素 (Shapes_Type complexType) (Visio XML)

**Master、Page、** またはグループ図形要素で図形を定義する要素を含む。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[図形](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |図形のコレクションを指定します。  <br/> |
|[図形](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |図形のコレクションを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1 つのプロパティを指定します。  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |図形に関する追加情報を提供するために使用される任意の文字列値を含む。  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |図形に関する追加情報を提供するために使用される任意の文字列値を含む。  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |図形に関する追加情報を提供するために使用される任意の文字列値を含む。  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |メタファイル、ビットマップ、OLE データなどの画像データの MIME (多目的インターネット メール拡張機能) エンコードされた BLOB がWindows含まれます。  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |関連するプロパティのコレクションを指定します。  <br/> |
|[図形](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |図形のコレクションを指定します。  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |図形のテキストが含まれます。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |省略可能  <br/> |要素がローカルで削除されるかどうかを示すフラグ。  <br/> |xsd:boolean 型の値。  <br/> |
|FillStyle  <br/> |xsd:unsignedInt  <br/> ||この図形が塗りつぶしの書式を継承する StyleSheet の ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親要素内の要素の一意の ID です。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |省略可能  <br/> |名前がユーザーによってカスタマイズされているかどうかを示します。  <br/> |xsd:boolean 型の値。  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |省略可能  <br/> |ユニバーサル名がユーザーによってカスタマイズされているかどうかを示します。  <br/> |xsd:boolean 型の値。  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> ||この図形が線の書式設定を継承する StyleSheet の ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |図形がデータを継承する Master 要素の ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|MasterShape  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |図形がデータを継承する Master 要素の ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の名前。  <br/> |xsd:string 型の値。  <br/> |
|NameU  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の汎用名。  <br/> |xsd:string 型の値。  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> ||この図形がテキストの書式設定を継承する StyleSheet の ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|種類  <br/> |xsd:token  <br/> |省略可能  <br/> |図形の種類。 グループ、図形、ガイド、または外部のいずれかの値を指定できます。  <br/> |xsd:token 型の値。  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |省略可能  <br/> |図形に割り当てられた GUID (グローバル一意識別子)。  <br/> |xsd:string 型の値。  <br/> |
   

