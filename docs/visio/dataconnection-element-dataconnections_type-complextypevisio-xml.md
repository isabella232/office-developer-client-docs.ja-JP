---
title: DataConnection 要素 (DataConnections_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: 1 つ以上の DataRecordset 要素と XML 以外のデータ ソースとの間の通信を抽象化します。
ms.openlocfilehash: c37c1076444febdc292fa91933b31f56413bc19e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563092"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a>DataConnection 要素 (DataConnections_Type complexType) (Visio XML)

1 つ以上の **DataRecordset** 要素と XML 以外のデータ ソースとの間の通信を抽象化します。 
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |connections.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |ドキュメントの **DataConnection** 要素を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd:boolean  <br/> |省略可能  <br/> |既定値は false です。 詳細については、「備考」を参照してください。  <br/> |xsd:boolean 型の値。  <br/> |
|Command  <br/> |xsd:string  <br/> |省略可能  <br/> |データ ソースのクエリに使用されるコマンド文字列。  <br/> |xsd:string 型の値。  <br/> |
|ConnectionString  <br/> |xsd:string  <br/> |省略可能  <br/> |データ ソースへの接続に必要なパラメーターを定義する接続文字列。  <br/> |xsd:string 型の値。  <br/> |
|FileName  <br/> |xsd:string  <br/> |必須  <br/> |接続ファイルの名前。 詳細については、「備考」を参照してください。  <br/> |xsd:string 型の値。  <br/> |
|FriendlyName  <br/> |xsd:string  <br/> |省略可能  <br/> |ユーザーがデータ接続の名前を指定しました。  <br/> |xsd:string 型の値。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |ドキュメント内で一意Visio接続に割り当てられた ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|Timeout  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |試行を終了する前に接続を確立しようとしている間の待機時間 (分)。  <br/> |xsd:unsignedInt 型の値。  <br/> |
   

