---
title: DataRecordSets 要素 (xml Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: ドキュメント内のすべての DataRecordset 要素を格納します。
ms.openlocfilehash: efa7d58eabc1b1192862dbbe090ddd5008947c1d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542444"
---
# <a name="datarecordsets-element-visio-xml"></a>DataRecordSets 要素 (xml Visio)

ドキュメント内のすべての **DataRecordset** 要素を格納します。 
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

なし。
  
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordset](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |ドキュメント内のすべての **DataRecordset** 要素を格納します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |ウィンドウが閉じると、[外部データ]ウィンドウ内のアクティブ なデータ レコードセットの ID が表示されます。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|DataWindowOrder  <br/> |xsd:string  <br/> |省略可能  <br/> |[外部データ] ウィンドウのタブに表示されるデータ レコードセット **の** 順序。 セミコロンで区切られたデータ レコードセットの ID の順序付きリスト。  <br/> |xsd:string 型の値。  <br/> |
|NextID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |新しいデータ レコードセットの次の使用可能な ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
   

