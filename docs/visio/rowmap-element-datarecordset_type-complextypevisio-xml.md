---
title: RowMap 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: データ レコードセットの行を図形にマップします。
ms.openlocfilehash: 250829c1199e4936bbdef91fdf3ba61873ff54fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607781"
---
# <a name="rowmap-element-datarecordset_type-complextype-visio-xml"></a>RowMap 要素 (DataRecordSet_Type complexType) (Visio XML)

データ レコードセットの行を図形にマップします。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

****

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordset](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Microsoft Visio で、データベースに対してクエリされたデータの保存、書式設定、更新、表示を行います。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |**RowID** で識別されるデータレコードセット行のデータにリンクされている図形のページ ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|RowID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |データレコードセット内の一意の行の ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |**RowID** で識別されるデータレコードセット行のデータにリンクされている図形の Shape ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
   

