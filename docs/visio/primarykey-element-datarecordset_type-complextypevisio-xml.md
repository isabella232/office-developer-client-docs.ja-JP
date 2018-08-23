---
title: 主キーの要素 (DataRecordSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: データ レコード セット内の 1 つまたは複数の主キー列を識別します。
ms.openlocfilehash: f720636bbdf2c55baca6d98aa7d0761607e53ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806119"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a>主キーの要素 (DataRecordSet_Type complexType)'Visio XML (')

データ レコード セット内の 1 つまたは複数の主キー列を識別します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[データ レコード セット](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[RowKeyValue](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |このコンポーネントのレコード セットの個別の行の主キーの値を指定します。 この子要素の 1 つ以上の出現が必要があります。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnNameID  <br/> |xsd:string  <br/> |省略可能  <br/> |主キーのコンポーネントであるフィールドの名前を指定します。 主キーが指定されている DataRecordSet_Type の DataColumn_Type の子孫要素の**ColumnNameID**属性の値である必要があります。  <br/> |Xsd:string の値を入力します。  <br/> |
   

