---
title: PrimaryKey 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: データ レコードセット内で 1 つ以上の主キー列を識別します。
ms.openlocfilehash: 3d537c0f8cf808da5ce8490fd584420b0a6e72b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627682"
---
# <a name="primarykey-element-datarecordset_type-complextype-visio-xml"></a>PrimaryKey 要素 (DataRecordSet_Type complexType) (Visio XML)

データ レコードセット内で 1 つ以上の主キー列を識別します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordset](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Microsoft Visio で、データベースに対してクエリされたデータの保存、書式設定、更新、表示を行います。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[RowKeyValue](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |レコードセットの個々の行の主キーのこのコンポーネントの値を指定します。 この子要素が少なくとも 1 つ出現する必要があります。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnNameID  <br/> |xsd:string  <br/> |省略可能  <br/> |主キーのコンポーネントであるフィールドの名前を指定します。 主キーが指定されているDataColumn_Typeの子要素DataRecordSet_Type **ColumnNameID** 属性の値である必要があります。  <br/> |xsd:string 型の値。  <br/> |
   

