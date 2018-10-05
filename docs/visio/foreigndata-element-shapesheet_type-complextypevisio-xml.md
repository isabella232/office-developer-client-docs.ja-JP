---
title: ForeignData 要素 (ShapeSheet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Windows メタファイル、ビットマップ、または OLE データなどの画像データの MIME (多目的インターネット メール拡張機能) のエンコードされた BLOB が含まれています。
ms.openlocfilehash: cce7665230fb9e68bf37002e1953944a5b8f8082
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382682"
---
# <a name="foreigndata-element-shapesheettype-complextype-visio-xml"></a>ForeignData 要素 (ShapeSheet_Type complexType)'Visio XML (')

Windows メタファイル、ビットマップ、または OLE データなどの画像データの MIME (多目的インターネット メール拡張機能) のエンコードされた BLOB が含まれています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |# .xml のページで、マスターの # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |**マスター シェイプ**、**ページ**、または図形要素のグループ内の図形を定義する要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |イメージ データを格納しているパーツとのリレーションシップを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |省略可能  <br/> |ファイルに適用する圧縮のレベルを指定します。 この属性は、意味のある外部データが、ラスター ベースの異物、DIB、JPG、PNG、TIFF、または GIF ファイルなどの場合のみです。  <br/> |Xsd:double 型の値です。  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |省略可能  <br/> |ファイルに適用する圧縮の種類を指定します。 この属性は外部データが、ラスター ベースの異物、DIB、JPG、PNG、TIFF、または GIF ファイルなどの場合は意味を持ちます。  <br/> |Xsd:token の値を入力します。  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |省略可能  <br/> |メタファイルの水平方向の範囲を指定します。 この属性は、意味のある外部データがメタファイルの場合のみです。  <br/> |Xsd:double 型の値です。  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |省略可能  <br/> |メタファイルの垂直方向のエクステントを指定します。 この属性は、意味のある外部データがメタファイルの場合のみです。  <br/> |Xsd:double 型の値です。  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |必須  <br/> |メタファイル、EnhMetaFile、ビットマップ、オブジェクト、またはインクの種類を示します。  <br/> |Xsd:token の値を入力します。  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |メタファイルのマップ モードを指定します。 この属性は、意味のある外部データがメタファイルの場合のみです。  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |省略可能  <br/> |ページの単位で、オブジェクトの高さを指定します。 この属性は、意味のある外部データが OLE2 埋め込みオブジェクトである場合のみです。  <br/> |Xsd:double 型の値です。  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |オブジェクト型の整数インジケーターです。 外部の型がオブジェクトである場合に使用されます。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |省略可能  <br/> |オブジェクトの幅をページ単位で指定します。 この属性は、意味のある外部データが OLE2 埋め込みオブジェクトである場合のみです。  <br/> |Xsd:double 型の値です。  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |省略可能  <br/> |表示または埋め込まれたデータをアイコンとして表示するかどうかを示します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
   

