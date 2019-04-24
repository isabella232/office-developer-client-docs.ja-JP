---
title: AutoLinkComparison 要素 (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: ユーザーインターフェイスで実行された前回正常に完了した自動リンクアクションの図形データ項目と親 DataRecordset 要素の列を比較するルールを定義します。
ms.openlocfilehash: 474acc4c1d259621881ea498decfeaf18b69809e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338319"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a>AutoLinkComparison 要素 (DataRecordSet_Type complexType) (' Visio XML ')

ユーザーインターフェイスで実行された前回正常に完了した自動リンクアクションの図形データ項目と親**DataRecordset**要素の列を比較するルールを定義します。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |recordsets  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |レコードセット、およびその recordset と図面ページの図形との間のデータバインドを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |xsd: string  <br/> |必須  <br/> |ADO recordset の列名に対応します。  <br/> |xsd: string 型の値。  <br/> |
|contexttype  <br/> |xsd: アン signedint  <br/> |必須  <br/> |比較に使用するグループまたは図形のプロパティを指定します。 使用可能な値を次の表に示します。  <br/> |xsd:/signedint 型の値。  <br/> |
|ContextTypeLabel  <br/> |xsd: string  <br/> |省略可能  <br/> |contexttype の値が2または3の場合、比較を定義するためにこの属性が必要になります。 contexttype = 2 の場合、ContextTypeLabel は図形データ項目のラベルである必要があります。 **contexttype** = 3 の場合は、ContextTypeLabel がローカルの行名である必要があります。  <br/> |xsd: string 型の値。  <br/> |
   

