---
title: 図形要素 (Shapes_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: マスター シェイプ、ページ、またはグループの図形要素の図形を定義する要素が含まれています。
ms.openlocfilehash: 8c0a288858e2aaccbd3afadcdc1b057565dd30ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806399"
---
# <a name="shape-element-shapestype-complextype-visio-xml"></a>図形要素 (Shapes_Type complexType)'Visio XML (')

**マスター シェイプ**、**ページ**、または図形要素のグループ内の図形を定義する要素が含まれています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |# .xml のページで、マスターの # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |図形のコレクションを指定します。  <br/> |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |図形のコレクションを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1 つのプロパティを指定します。  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |図形に関する追加情報を提供するために使用される任意の文字列値が含まれています。  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |図形に関する追加情報を提供するために使用される任意の文字列値が含まれています。  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |図形に関する追加情報を提供するために使用される任意の文字列値が含まれています。  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Windows メタファイル、ビットマップ、または OLE データなどの画像データの MIME (多目的インターネット メール拡張機能) のエンコードされた BLOB が含まれています。  <br/> |
|[セクション](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |関連するプロパティのコレクションを指定します。  <br/> |
|[Shapes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |図形のコレクションを指定します。  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |図形のテキストが含まれています。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |省略可能  <br/> |要素がローカルで削除するかどうかを示すフラグです。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|FillStyle  <br/> |xsd:unsignedInt  <br/> ||この図形の継承元の塗りつぶしの書式設定スタイル シートの ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |その親要素内の要素の一意の ID。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |省略可能  <br/> |名前がユーザーによってカスタマイズされているかどうかを示します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |省略可能  <br/> |汎用名がユーザーによってカスタマイズされているかどうかを示します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> ||この図形の継承元の行の書式設定スタイル シートの ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |マスターの ID 要素は、図形のデータを継承します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|MasterShape  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |マスターの ID 要素は、図形のデータを継承します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の名前です。  <br/> |Xsd:string の値を入力します。  <br/> |
|NameU  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の汎用名です。  <br/> |Xsd:string の値を入力します。  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> ||この図形の継承元のテキストの書式設定スタイル シートの ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|型  <br/> |xsd:token  <br/> |省略可能  <br/> |図形の種類。 次の値の 1 つがあります: グループ、図形、ガイド、または外部。  <br/> |Xsd:token の値を入力します。  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |省略可能  <br/> |図形に割り当てられた GUID (グローバル一意識別子) です。  <br/> |Xsd:string の値を入力します。  <br/> |
   

