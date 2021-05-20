---
title: ForeignData 要素 (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: メタファイル、ビットマップ、OLE データなどの画像データの MIME (多目的インターネット メール拡張機能) エンコードされた BLOB がWindows含まれます。
ms.openlocfilehash: 6b130b5a50a51d5d909b843e805d197735dc7146
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539843"
---
# <a name="foreigndata-element-shapesheet_type-complextype-visio-xml"></a>ForeignData 要素 (ShapeSheet_Type complexType) (Visio XML)

メタファイル、ビットマップ、OLE データなどの画像データの MIME (多目的インターネット メール拡張機能) エンコードされた BLOB がWindows含まれます。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |**Master、Page、** またはグループ図形要素で図形を定義する要素を含む。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |イメージ データを含むパーツとの関係を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |省略可能  <br/> |ファイルに適用される圧縮のレベルを指定します。 この属性は、外部データがラスター ベースの外部オブジェクト (DIB、JPG、PNG、TIFF、GIF ファイルなど) である場合にのみ意味があります。  <br/> |xsd:double 型の値。  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |省略可能  <br/> |ファイルに適用される圧縮の種類を指定します。 この属性は、外部データがラスター ベースの外部オブジェクト (DIB、JPG、PNG、TIFF、GIF ファイルなど) の場合にのみ意味があります。  <br/> |xsd:token 型の値。  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |省略可能  <br/> |メタファイルの水平方向の範囲を指定します。 この属性は、外部データがメタファイルである場合にのみ意味があります。  <br/> |xsd:double 型の値。  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |省略可能  <br/> |メタファイルの垂直方向の範囲を指定します。 この属性は、外部データがメタファイルである場合にのみ意味があります。  <br/> |xsd:double 型の値。  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |必須  <br/> |メタファイル、EnhMetaFile、Bitmap、Object、または Ink の種類を示します。  <br/> |xsd:token 型の値。  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |メタファイル マッピング モードを指定します。 この属性は、外部データがメタファイルである場合にのみ意味があります。  <br/> |xsd:unsignedShort 型の値。  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |省略可能  <br/> |オブジェクトの高さをページ単位で指定します。 この属性は、外部データが OLE2 埋め込みオブジェクトである場合にのみ意味があります。  <br/> |xsd:double 型の値。  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |オブジェクトの種類の整数インジケーター。 外部型がオブジェクトの場合に使用されます。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |省略可能  <br/> |オブジェクトの幅をページ単位で指定します。 この属性は、外部データが OLE2 埋め込みオブジェクトである場合にのみ意味があります。  <br/> |xsd:double 型の値。  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |省略可能  <br/> |埋め込みデータをアイコンとして表示するかどうかを示します。  <br/> |xsd:boolean 型の値。  <br/> |
   

