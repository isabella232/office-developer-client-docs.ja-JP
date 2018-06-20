---
title: DataRecordSets 要素 ' Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: ドキュメント内にあるデータ レコード セットのすべての要素が含まれています。
ms.openlocfilehash: 205c4d963f111490698627040c190f322f2f36a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805169"
---
# <a name="datarecordsets-element-visio-xml"></a>DataRecordSets 要素 ' Visio XML (')

ドキュメント内にある**データ レコード セット**のすべての要素が含まれています。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

なし。
  
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[データ レコード セット](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |ドキュメント内にある**データ レコード セット**のすべての要素が含まれています。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |ウィンドウが閉じて、ことができるように、次回ウィンドウが復元されたときは、[**外部データ**] ウィンドウで作業中のデータ レコード セットの ID が表示されます。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|DataWindowOrder  <br/> |xsd:string  <br/> |省略可能  <br/> |**外部データ**ウィンドウのタブに表示するデータ レコード セットの順序です。 セミコロンで区切られたデータ レコード セット Id の順序付きリストです。  <br/> |Xsd:string の値を入力します。  <br/> |
|NextID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |新しいデータ レコード セットの次の使用可能な ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
   

