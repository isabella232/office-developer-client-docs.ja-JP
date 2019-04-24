---
title: DataRecordSets 要素 (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: 文書内のすべての DataRecordset 要素が含まれています。
ms.openlocfilehash: 7730e55f0025181db193a1e64226e879f9072e90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360327"
---
# <a name="datarecordsets-element-visio-xml"></a>DataRecordSets 要素 (' Visio XML ')

文書内のすべての**DataRecordset**要素が含まれています。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |recordsets  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

なし。
  
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |文書内のすべての**DataRecordset**要素が含まれています。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |ウィンドウが閉じているときに、[**外部データ**] ウィンドウのアクティブなデータレコードセットの ID を指定します。その後、次回ウィンドウを開いたときに復元できるようになります。  <br/> |xsd:/signedint 型の値。  <br/> |
|DataWindowOrder  <br/> |xsd: string  <br/> |省略可能  <br/> |[**外部データ**] ウィンドウのタブに表示されるデータレコードセットの順序です。 データレコードセット id の順序付きリスト。セミコロンで区切られています。  <br/> |xsd: string 型の値。  <br/> |
|NextID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |新しいデータレコードセットに対して使用可能な次の ID。  <br/> |xsd:/signedint 型の値。  <br/> |
   

