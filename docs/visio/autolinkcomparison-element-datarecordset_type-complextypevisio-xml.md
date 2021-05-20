---
title: AutoLinkComparison 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: ユーザー インターフェイスで最後に正常に実行された自動リンク アクションからの図形データ アイテムと、親 DataRecordset 要素内の列を比較するルールを定義します。
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537872"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a>AutoLinkComparison 要素 (DataRecordSet_Type complexType) (Visio XML)

ユーザー インターフェイスで最後に正常に実行された自動リンク アクションからの図形データ アイテムと、親 **DataRecordset** 要素内の列を比較するルールを定義します。 
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordset](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |図面ページ内のレコードセットと図形間のレコードセットとデータ バインドを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |xsd:string  <br/> |必須  <br/> |ADO レコードセット内の列名に対応します。  <br/> |xsd:string 型の値。  <br/> |
|ContextType  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |比較に使用するグループまたは図形のプロパティを指定します。 使用できる値を次の表に示します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ContextTypeLabel  <br/> |xsd:string  <br/> |省略可能  <br/> |ContextType 値が 2 または 3 の場合、比較を定義するには、この属性が必要です。 ContextType = 2 の場合、ContextTypeLabel は図形データ項目ラベルである必要があります **。ContextType** = 3 の場合、ContextTypeLabel はローカル行名である必要があります。  <br/> |xsd:string 型の値。  <br/> |
   

