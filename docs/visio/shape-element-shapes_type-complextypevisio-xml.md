---
title: Shape 要素 (Shapes_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: マスターシェイプ、ページ、またはグループの shape 要素の図形を定義する要素が含まれます。
ms.openlocfilehash: aa7ffa539c9f82adc486bd0848dda66798bac165
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542073"
---
# <a name="shape-element-shapestype-complextype-visio-xml"></a>Shape 要素 (Shapes_Type complexType) (Visio XML)

**マスター**シェイプ、**ページ**、またはグループの shape 要素の図形を定義する要素が含まれます。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |ページ # .xml、マスター # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |図形のコレクションを指定します。  <br/> |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |図形のコレクションを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1つのプロパティを指定します。  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |図形に関する追加情報を提供するために使用される任意の文字列値を格納します。  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |図形に関する追加情報を提供するために使用される任意の文字列値を格納します。  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |図形に関する追加情報を提供するために使用される任意の文字列値を格納します。  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Windows メタファイル、ビットマップ、OLE データなど、画像データの MIME (多目的インターネットメール内線) でエンコードされた BLOB を格納します。  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |関連するプロパティのコレクションを指定します。  <br/> |
|[Shapes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |図形のコレクションを指定します。  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |図形のテキストを格納します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd: boolean  <br/> |省略可能  <br/> |要素がローカルで削除されるかどうかを示すフラグ。  <br/> |Xsd: boolean 型の値。  <br/> |
|FillStyle  <br/> |xsd: アン Signedint  <br/> ||この図形が塗りつぶしの書式設定を継承するスタイルシートの ID です。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|ID  <br/> |xsd: アン Signedint  <br/> |必須  <br/> |親要素内の要素の一意の ID。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|IsCustomName  <br/> |xsd: boolean  <br/> |省略可能  <br/> |ユーザーによって名前がカスタマイズされているかどうかを示します。  <br/> |Xsd: boolean 型の値。  <br/> |
|IsCustomNameU  <br/> |xsd: boolean  <br/> |省略可能  <br/> |ユーザーによって汎用名がカスタマイズされているかどうかを示します。  <br/> |Xsd: boolean 型の値。  <br/> |
|LineStyle  <br/> |xsd: アン Signedint  <br/> ||この図形が線の書式設定を継承するスタイルシートの ID です。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|Master  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |図形のデータを継承するマスター要素の ID。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|MasterShape  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |図形のデータを継承するマスター要素の ID。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> |要素の名前。  <br/> |Xsd: string 型の値。  <br/> |
|NameU  <br/> |xsd: string  <br/> |省略可能  <br/> |要素の汎用名。  <br/> |Xsd: string 型の値。  <br/> |
|TextStyle  <br/> |xsd: アン Signedint  <br/> ||この図形がテキストの書式設定を継承するスタイルシートの ID です。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|型  <br/> |xsd: token  <br/> |省略可能  <br/> |図形の種類を示します。 グループ、図形、ガイド、または外部のいずれかの値を指定できます。  <br/> |Xsd: token 型の値。  <br/> |
|UniqueID  <br/> |xsd: string  <br/> |省略可能  <br/> |図形に割り当てられた GUID (グローバル一意識別子)。  <br/> |Xsd: string 型の値。  <br/> |
   

