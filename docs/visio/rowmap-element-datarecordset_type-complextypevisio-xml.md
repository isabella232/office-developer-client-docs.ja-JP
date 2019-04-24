---
title: rowmap 要素 (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: データレコードセットの行を図形にマップします。
ms.openlocfilehash: 2dffa49d66e8e447b4e31d771179c74eecad21da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332516"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a>rowmap 要素 (DataRecordSet_Type complexType) (' Visio XML ')

データレコードセットの行を図形にマップします。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |recordsets  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

****

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |**RowID**で識別されるデータレコードセット行のデータにリンクされている図形のページ ID。  <br/> |xsd:/signedint 型の値。  <br/> |
|RowID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |データレコードセット内で一意の行 ID。  <br/> |xsd:/signedint 型の値。  <br/> |
|ShapeID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |**RowID**で識別されるデータレコードセット行のデータにリンクされている図形の図形 ID。  <br/> |xsd:/signedint 型の値。  <br/> |
   

