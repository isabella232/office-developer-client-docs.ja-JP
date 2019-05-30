---
title: ForeignData 要素 (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Windows メタファイル、ビットマップ、OLE データなど、画像データの MIME (多目的インターネットメール内線) でエンコードされた BLOB を格納します。
ms.openlocfilehash: 6b130b5a50a51d5d909b843e805d197735dc7146
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539843"
---
# <a name="foreigndata-element-shapesheettype-complextype-visio-xml"></a>ForeignData 要素 (ShapeSheet_Type complexType) (Visio XML)

Windows メタファイル、ビットマップ、OLE データなど、画像データの MIME (多目的インターネットメール内線) でエンコードされた BLOB を格納します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |ページ # .xml、マスター # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |**マスター**シェイプ、**ページ**、またはグループの shape 要素の図形を定義する要素が含まれます。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |画像データを含むパーツへのリレーションシップを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd: double  <br/> |省略可能  <br/> |ファイルに適用される圧縮レベルを指定します。 この属性は、外部データが、DIB、JPG、PNG、TIFF、GIF ファイルなどのラスターベースの外部オブジェクトである場合にのみ意味があります。  <br/> |Xsd: double 型の値。  <br/> |
|CompressionType  <br/> |xsd: token  <br/> |省略可能  <br/> |ファイルに適用される圧縮の種類を指定します。 この属性は、外部データが、DIB、JPG、PNG、TIFF、GIF ファイルなどのラスターベースの外部オブジェクトである場合にのみ意味があります。  <br/> |Xsd: token 型の値。  <br/> |
|ExtentX  <br/> |xsd: double  <br/> |省略可能  <br/> |メタファイルの水平方向のエクステントを指定します。 この属性は、外部データがメタファイルの場合にのみ意味があります。  <br/> |Xsd: double 型の値。  <br/> |
|ExtentY  <br/> |xsd: double  <br/> |省略可能  <br/> |メタファイルの垂直方向のエクステントを指定します。 この属性は、外部データがメタファイルの場合にのみ意味があります。  <br/> |Xsd: double 型の値。  <br/> |
|ForeignType  <br/> |xsd: token  <br/> |必須  <br/> |メタファイル、EnhMetaFile、Bitmap、Object、または Ink の種類を示します。  <br/> |Xsd: token 型の値。  <br/> |
|MappingMode  <br/> |xsd: アン Signedshort  <br/> |省略可能  <br/> |メタファイルマッピングモードを指定します。 この属性は、外部データがメタファイルの場合にのみ意味があります。  <br/> |Xsd: _ Signedshort 型の値。  <br/> |
|ObjectHeight  <br/> |xsd: double  <br/> |省略可能  <br/> |オブジェクトの高さをページ単位で指定します。 この属性は、外部データが OLE2 埋め込みオブジェクトである場合にのみ意味を持ちます。  <br/> |Xsd: double 型の値。  <br/> |
|ObjectType  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |オブジェクトの種類の整数インジケーター。 外部型が object の場合に使用します。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|ObjectWidth  <br/> |xsd: double  <br/> |省略可能  <br/> |オブジェクトの幅をページ単位で指定します。 この属性は、外部データが OLE2 埋め込みオブジェクトである場合にのみ意味を持ちます。  <br/> |Xsd: double 型の値。  <br/> |
|ShowAsIcon  <br/> |xsd: boolean  <br/> |省略可能  <br/> |埋め込みデータをアイコンとして表示するかどうかを示します。  <br/> |Xsd: boolean 型の値。  <br/> |
   

