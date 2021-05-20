---
title: Rel 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: 関連付けられたレコードセットとデータ バインド情報を持つパーツとの関係を指定します。
ms.openlocfilehash: fa93a3cbc32b6929b159b958ef2a96eafacf204f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542864"
---
# <a name="rel-element-datarecordset_type-complextype-visio-xml"></a>Rel 要素 (DataRecordSet_Type complexType) (Visio XML)

関連付けられたレコードセットとデータ バインド情報を持つパーツとの関係を指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |pages.xml、masters.xml、recordsets.xml、page#.xml、master#.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordset](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |図面に格納されているレコードセットとデータ バインド情報の 1 つのインスタンスを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|r:id  <br/> |xsd:string  <br/> 注釈を参照してください。  <br/> |必須  <br/> |パーツとの関係を指定します。  <br/> |"rId#"  <br/> 注釈を参照してください。  <br/> |
   
## <a name="remarks"></a>注釈

**r:id 属性の値** は、次の型 **ST_RelationshipID** があります。 この **ST_RelationshipID** は、'rId#' 形式である必要がある文字列で、最後の文字は数値である必要があります。 この数値は **、Rel** 要素のすべての兄弟要素間で一意である必要があります。 
  
この種類の詳細ST_RelationshipID [ISO/IEC 29500 パート 1 の仕様を参照してください](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)。
  

