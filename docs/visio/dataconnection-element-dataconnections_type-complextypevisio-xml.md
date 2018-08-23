---
title: DataConnection 要素 (DataConnections_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: 1 つまたは複数のデータ レコード セットの要素と XML 以外のデータ ソース間の通信を抽象化します。
ms.openlocfilehash: 74e15795e023517263d9b79e9f19557653e4e939
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805174"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a>DataConnection 要素 (DataConnections_Type complexType)'Visio XML (')

1 つまたは複数の**データ レコード セット**の要素と XML 以外のデータ ソース間の通信を抽象化します。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |connections.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |ドキュメントの**DataConnection**要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd:boolean  <br/> |省略可能  <br/> |既定値は、false を指定します。 詳細については、「備考」を参照してください。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|コマンド  <br/> |xsd:string  <br/> |省略可能  <br/> |コマンド文字列は、データ ソースのクエリを実行するために使用します。  <br/> |Xsd:string の値を入力します。  <br/> |
|ConnectionString  <br/> |xsd:string  <br/> |省略可能  <br/> |データ ソースに接続するために必要なパラメーターを定義する接続文字列です。  <br/> |Xsd:string の値を入力します。  <br/> |
|FileName  <br/> |xsd:string  <br/> |必須  <br/> |接続ファイルの名前です。 詳細については、「備考」を参照してください。  <br/> |Xsd:string の値を入力します。  <br/> |
|FriendlyName  <br/> |xsd:string  <br/> |省略可能  <br/> |ユーザーは、データ接続の名前を提供します。  <br/> |Xsd:string の値を入力します。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |Visio で指定された接続では、ドキュメント内で一意に割り当てられた ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|Timeout  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |試行を終了する前に接続を確立しようとしているときに分単位での待機時間です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
   

