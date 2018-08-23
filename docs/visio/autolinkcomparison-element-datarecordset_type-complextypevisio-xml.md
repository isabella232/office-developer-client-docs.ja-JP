---
title: AutoLinkComparison 要素 (DataRecordSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: 前回成功した自動リンクで実行されたアクション ユーザー インターフェイスからの図形データ項目の親データ レコード セットの要素内の列を比較するルールを定義します。
ms.openlocfilehash: 38970a84676f769c36c9bdc3f8334652f7d9ec21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804800"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a>AutoLinkComparison 要素 (DataRecordSet_Type complexType)'Visio XML (')

前回成功した自動リンクで実行されたアクション ユーザー インターフェイスからの図形データ項目の親**データ レコード セット**の要素内の列を比較するルールを定義します。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[データ レコード セット](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |図面ページで、レコード セットとそのレコード セットと図形間のデータ バインディングを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |xsd:string  <br/> |必須  <br/> |ADO レコード セット内の列名に対応します。  <br/> |Xsd:string の値を入力します。  <br/> |
|ContextType  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |比較に使用するには、グループまたは図形のプロパティを指定します。 使用可能な値は、次の表に表示されます。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ContextTypeLabel  <br/> |xsd:string  <br/> |省略可能  <br/> |ContextType の値が 2 または 3 の場合は、比較を定義するのにはこの属性が必要です。 ContextType = 2、ContextTypeLabel は、図形データ アイテムのラベルをして、場合必要があります。 **ContextType** = 3、ContextTypeLabel は、ローカル行の名前をする必要があります。  <br/> |Xsd:string の値を入力します。  <br/> |
   

