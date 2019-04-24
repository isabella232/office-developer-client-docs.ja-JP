---
title: PrimaryKey 要素 (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: データレコードセット内の1つまたは複数の主キー列を指定します。
ms.openlocfilehash: c001c343c33e65c3990744b885f1c345575b1ab3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355997"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a>PrimaryKey 要素 (DataRecordSet_Type complexType) (' Visio XML ')

データレコードセット内の1つまたは複数の主キー列を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |recordsets  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[rowkeyvalue](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |recordset の個々の行の主キーのこのコンポーネントの値を指定します。 少なくとも1つの子要素が存在する必要があります。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|columnnameid  <br/> |xsd: string  <br/> |省略可能  <br/> |主キーのコンポーネントであるフィールドの名前を指定します。 主キーが指定されている DataRecordSet_Type の DataColumn_Type 子孫要素の**columnnameid**属性の値である必要があります。  <br/> |xsd: string 型の値。  <br/> |
   

