---
title: DataColumn の要素 (DataColumns_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: データ列が Visio ユーザー インターフェイスの [外部データ] ウィンドウで表示する方法を定義し、そのデータ型を定義して、書式設定、列のデータが適用されます。
ms.openlocfilehash: f74061b9f3b8f4b93d8aa0e97e4e7c1e45131cbd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805180"
---
# <a name="datacolumn-element-datacolumnstype-complextype-visio-xml"></a>DataColumn の要素 (DataColumns_Type complexType)'Visio XML (')

データ列が Visio ユーザー インターフェイスの [**外部データ**] ウィンドウで表示する方法を定義し、そのデータ型を定義して、書式設定、列のデータが適用されます。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Datacolumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |データ レコード セット内のすべての**列**要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|カレンダー  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |データ列の予定表の ID です。  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|ColumnNameID  <br/> |xsd:string  <br/> |必須  <br/> |データ列の外部名。 [**外部データ**] ウィンドウおよび [データ グラフィックのラベルでは、見出しに表示されます。  <br/> |Xsd:string の値を入力します。  <br/> |
|通貨型 (Currency)  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |データ列の通貨の ID です。  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |データ列内のデータの種類です。  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|度  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |単位、たとえば、乗、2 乗の程度 (電源) を指定します。 既定値 (省略可能な属性) とは、1 です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|DisplayOrder  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |(最大値) の右端の列の一番左の列 (0) から、**外部データ**ウィンドウでデータ列の表示位置を定義します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |[**外部データ**] ウィンドウで [データ] 列の幅です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ハイパーリンク  <br/> |xsd:boolean  <br/> |省略可能  <br/> |かどうか、データ列は、図形がデータにリンクされている場合、図形にハイパーリンクを作成します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|ラベル  <br/> |xsd:string  <br/> |必須  <br/> |データ列のラベルです。  <br/> |Xsd:string の値を入力します。  <br/> |
|LangID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |データ列の言語 ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|マップ  <br/> |xsd:boolean  <br/> |省略可能  <br/> |[**外部データ**] ウィンドウの列が表示されているかどうかを指定します。 表示されている列の true (1)列を表示するのには false (0)。 (省略可能な属性) の既定値は、列を表示するは。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |必須  <br/> |データ列の内部名です。 図形がデータ行にリンクされている場合、図形に追加された図形データ項目 (カスタム プロパティ) の行の名前として使用されます。  <br/> |Xsd:string の値を入力します。  <br/> |
|OrigLabel  <br/> |xsd:string  <br/> |省略可能  <br/> |列ラベルの基になる ADO インターフェイスによって、Visio に返されます。  <br/> |Xsd:string の値を入力します。  <br/> |
|UnitType  <br/> |xsd:string  <br/> |省略可能  <br/> |データ列内のデータの単位のタイプ。  <br/> |Xsd:string の値を入力します。  <br/> |
   

