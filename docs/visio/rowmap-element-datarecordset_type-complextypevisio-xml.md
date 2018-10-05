---
title: RowMap 要素 (DataRecordSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: レコード セットのデータ行を図形にマップします。
ms.openlocfilehash: 2dffa49d66e8e447b4e31d771179c74eecad21da
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385313"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a>RowMap 要素 (DataRecordSet_Type complexType)'Visio XML (')

レコード セットのデータ行を図形にマップします。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

****

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[データ レコード セット](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |**RowID**で識別されるデータ レコード セット行のデータにリンクされている図形のページの ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|RowID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |データ レコード セット内で一意の行の行 ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |**RowID**で識別されるデータ レコード セット行のデータにリンクされた図形の図形 ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
   

