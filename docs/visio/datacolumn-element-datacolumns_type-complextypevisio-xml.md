---
title: DataColumn 要素 (DataColumns_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Visio ユーザーインターフェイスの [外部データ] ウィンドウにデータ列を表示する方法を定義し、データの種類と書式を定義することによって、列のデータを修飾します。
ms.openlocfilehash: 453ff44131575bd3d6927fdddb81db5f3f431a3b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344822"
---
# <a name="datacolumn-element-datacolumnstype-complextype-visio-xml"></a>DataColumn 要素 (DataColumns_Type complexType) (' Visio XML ')

Visio ユーザーインターフェイスの [**外部データ**] ウィンドウにデータ列を表示する方法を定義し、データの種類と書式を定義することによって、列のデータを修飾します。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |recordsets  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |データレコードセット内のすべての**DataColumn**要素を含みます。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|カレンダー  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> |データ列のカレンダー ID。  <br/> |xsd: _ signedshort 型の値。  <br/> |
|columnnameid  <br/> |xsd: string  <br/> |必須  <br/> |データ列の外部名。 [**外部データ**] ウィンドウの見出し、および [データグラフィック] のラベルに表示されます。  <br/> |xsd: string 型の値。  <br/> |
|通貨  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> |データ列の通貨 ID。  <br/> |xsd: _ signedshort 型の値。  <br/> |
|DataType  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> |データ列のデータの種類。  <br/> |xsd: _ signedshort 型の値。  <br/> |
|Degree  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |単位の角度 (累乗) を指定します。たとえば、平方または cubed を指定します。 既定値 (省略した属性) は1です。  <br/> |xsd:/signedint 型の値。  <br/> |
|displayorder  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |[**外部データ**] ウィンドウで、左端の列 (0) から右端の列 (最大値) までのデータ列の表示位置を定義します。  <br/> |xsd:/signedint 型の値。  <br/> |
|displaywidth  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |[**外部データ**] ウィンドウのデータ列の幅。  <br/> |xsd:/signedint 型の値。  <br/> |
|Hyperlink  <br/> |xsd: boolean  <br/> |省略可能  <br/> |図形がデータにリンクされているときに、データ列が図形にハイパーリンクを作成するかどうかを指定します。  <br/> |xsd: boolean 型の値。  <br/> |
|Label  <br/> |xsd: string  <br/> |必須  <br/> |データ列のラベル。  <br/> |xsd: string 型の値。  <br/> |
|LangID  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |データ列の言語 ID。  <br/> |xsd:/signedint 型の値。  <br/> |
|変換  <br/> |xsd: boolean  <br/> |省略可能  <br/> |[**外部データ**] ウィンドウに列を表示するかどうかを指定します。 表示する列の場合は True (1)。列が表示されないようにするには、False (0) を指定します。 既定値 (省略可能) は、列を表示するためのものです。  <br/> |xsd: boolean 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |必須  <br/> |データ列の内部名。 図形がデータ行にリンクされている場合に、図形に追加された図形データ項目 (カスタムプロパティ) の行名として使用されます。  <br/> |xsd: string 型の値。  <br/> |
|OrigLabel  <br/> |xsd: string  <br/> |省略可能  <br/> |基になる ADO インターフェイスで Visio に返される列ラベル。  <br/> |xsd: string 型の値。  <br/> |
|UnitType  <br/> |xsd: string  <br/> |省略可能  <br/> |データ列のデータの単位の種類。  <br/> |xsd: string 型の値。  <br/> |
   

