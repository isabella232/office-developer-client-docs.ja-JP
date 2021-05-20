---
title: DataColumn 要素 (DataColumns_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Visio ユーザー インターフェイスの [外部データ] ウィンドウにデータ列を表示する方法を定義し、データ型と書式を定義することで列内のデータを修飾します。
ms.openlocfilehash: 021e7ffd154f1e124b9eb163acc27260b90c23eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541226"
---
# <a name="datacolumn-element-datacolumns_type-complextype-visio-xml"></a>DataColumn 要素 (DataColumns_Type complexType) (Visio XML)

Visio ユーザー インターフェイスの **[外部データ]** ウィンドウにデータ列を表示する方法を定義し、データ型と書式を定義することで列内のデータを修飾します。 
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |データ レコードセット内のすべての **DataColumn** 要素を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|予定表  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |データ列の予定表 ID。  <br/> |xsd:unsignedShort 型の値。  <br/> |
|ColumnNameID  <br/> |xsd:string  <br/> |必須  <br/> |データ列の外部名。 [外部データ] ウィンドウの見出しとデータ グラフィックスのラベルに表示されます。  <br/> |xsd:string 型の値。  <br/> |
|通貨  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |データ列の通貨 ID。  <br/> |xsd:unsignedShort 型の値。  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |データ列のデータの種類。  <br/> |xsd:unsignedShort 型の値。  <br/> |
|Degree  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |単位の次数 (乗数) を指定します (二乗、立方体など)。 既定値 (属性が存在しない) は 1 です。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|DisplayOrder  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |[外部データ] ウィンドウのデータ列の表示位置を、最も左の列 (0) から最も右の列 (最大の値) に定義します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |[外部データ] ウィンドウのデータ **列の幅** 。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ハイパーリンク  <br/> |xsd:boolean  <br/> |省略可能  <br/> |データ列がデータにリンクされている図形にハイパーリンクを作成するかどうかを指定します。  <br/> |xsd:boolean 型の値。  <br/> |
|ラベル  <br/> |xsd:string  <br/> |必須  <br/> |データ列のラベル。  <br/> |xsd:string 型の値。  <br/> |
|LangID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |データ列の言語 ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|マッピングされた  <br/> |xsd:boolean  <br/> |省略可能  <br/> |[外部データ] ウィンドウに列を表示するかどうかを **指定** します。 列を表示するには True (1) を指定します。列が表示されない場合は False (0) です。 列を表示するには、既定の (属性が存在しません)。  <br/> |xsd:boolean 型の値。  <br/> |
|名前  <br/> |xsd:string  <br/> |必須  <br/> |データ列の内部名。 図形がデータ行にリンクされているときに図形に追加される図形データ項目 (カスタム プロパティ) の行名として使用されます。  <br/> |xsd:string 型の値。  <br/> |
|OrigLabel  <br/> |xsd:string  <br/> |省略可能  <br/> |基になる ADO インターフェイスVisioに返される列ラベル。  <br/> |xsd:string 型の値。  <br/> |
|UnitType  <br/> |xsd:string  <br/> |省略可能  <br/> |データ列内のデータの単位の種類。  <br/> |xsd:string 型の値。  <br/> |
   

