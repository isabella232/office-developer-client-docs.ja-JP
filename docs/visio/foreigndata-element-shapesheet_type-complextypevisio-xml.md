---
title: ForeignData 要素 (ShapeSheet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Windows メタファイル、ビットマップ、OLE データなどの画像データの MIME (多目的インターネットメール拡張機能) エンコード済み BLOB が含まれます。
ms.openlocfilehash: cce7665230fb9e68bf37002e1953944a5b8f8082
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346033"
---
# <a name="foreigndata-element-shapesheettype-complextype-visio-xml"></a>ForeignData 要素 (ShapeSheet_Type complexType) ('Visio XML')

Windows メタファイル、ビットマップ、OLE データなどの画像データの MIME (多目的インターネットメール拡張機能) エンコード済み BLOB が含まれます。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |**Master**、**Page** またはグループの図形要素の図形を定義する要素を含みます。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |画像データを含む部分のリレーションシップを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |省略可能  <br/> |ファイルに適用されている圧縮レベルを指定します。 この属性は、外部データが DIB、JPG、PNG、TIFF、GIF ファイルなど、ラスターベースの外部オブジェクトの場合にのみ意味を持ちます。  <br/> |xsd:double 型の値。  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |省略可能  <br/> |ファイルに適用されている圧縮タイプを指定します。 この属性は、外部データが DIB、JPG、PNG、TIFF、GIF ファイルなど、ラスターベースの外部オブジェクトの場合にのみ意味を持ちます。  <br/> |xsd:token 型の値。  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |省略可能  <br/> |メタファイルの横方向の範囲を指定します。 この属性は、外部データがメタファイルの場合にのみ意味を持ちます。  <br/> |xsd:double 型の値。  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |省略可能  <br/> |メタファイルの縦方向の範囲を指定します。 この属性は、外部データがメタファイルの場合にのみ意味を持ちます。  <br/> |xsd:double 型の値。  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |必須  <br/> |Metafile、EnhMetaFile、Bitmap、Object、またはインクの種類を示します。  <br/> |xsd:token 型の値。  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |メタファイルのマッピングモードを指定します。 この属性は、外部データがメタファイルの場合にのみ意味を持ちます。  <br/> |xsd:unsignedShort 型の値。  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |省略可能  <br/> |オブジェクトの高さをページ単位で指定します。 この属性は、外部データが OLE2 埋め込みオブジェクトの場合にのみ意味を持ちます。  <br/> |xsd:double 型の値。  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |オブジェクトの種類の整数インジケーター。 外部タイプがオブジェクトの場合に使用されます。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |省略可能  <br/> |オブジェクトの幅をページ単位で指定します。 この属性は、外部データが OLE2 埋め込みオブジェクトの場合にのみ意味を持ちます。  <br/> |xsd:double 型の値。  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |省略可能  <br/> |埋め込みデータをアイコンとして表示するかどうかを示します。  <br/> |xsd:boolean 型の値。  <br/> |
   

