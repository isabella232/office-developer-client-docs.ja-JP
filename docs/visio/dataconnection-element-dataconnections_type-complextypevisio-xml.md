---
title: DataConnection 要素 (DataConnections_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: 1つまたは複数の DataRecordset 要素と非 XML データソース間の情報を抽出します。
ms.openlocfilehash: 0073c329ec9149263530421531522c4d0b95633d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344626"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a>DataConnection 要素 (DataConnections_Type complexType) (' Visio XML ')

1つまたは複数の**DataRecordset**要素と非 XML データソース間の情報を抽出します。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |接続 xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |文書の**DataConnection**要素を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd: boolean  <br/> |省略可能  <br/> |既定値は false です。 詳細については、「備考」を参照してください。  <br/> |xsd: boolean 型の値。  <br/> |
|Command  <br/> |xsd: string  <br/> |省略可能  <br/> |データソースのクエリに使用されるコマンド文字列。  <br/> |xsd: string 型の値。  <br/> |
|ConnectionString  <br/> |xsd: string  <br/> |省略可能  <br/> |データソースへの接続に必要なパラメーターを定義する接続文字列。  <br/> |xsd: string 型の値。  <br/> |
|FileName  <br/> |xsd: string  <br/> |必須  <br/> |接続ファイルの名前を指定します。 詳細については、「備考」を参照してください。  <br/> |xsd: string 型の値。  <br/> |
|FriendlyName  <br/> |xsd: string  <br/> |省略可能  <br/> |ユーザーが入力したデータ接続の名前。  <br/> |xsd: string 型の値。  <br/> |
|ID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |指定された接続に対して Visio によって割り当てられた ID。ドキュメント内で一意です。  <br/> |xsd:/signedint 型の値。  <br/> |
|Timeout  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |試行を終了する前に接続を確立しようとしている間の待機時間 (分単位)。  <br/> |xsd:/signedint 型の値。  <br/> |
   

