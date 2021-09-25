---
title: DataSource プロパティ (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ffb7d6990c19dd0abb0efc572eadb95bdfb7f9c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558465"
---
# <a name="datasource-property-ado"></a>DataSource プロパティ (ADO)


**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクトとして表されるデータを持つオブジェクトを示します。

## <a name="remarks"></a>注釈

This property is used to create data-bound controls with the Data Environment. Data Environment は、Recordset オブジェクトとして表される名前付きオブジェクト *(データ* メンバー) を含むデータ (データ ソース) のコレクション **を保持** します *。*

[DataMember](datamember-property-ado.md) プロパティと **DataSource** プロパティは組み合わせて使用する必要があります。

参照されるオブジェクトには、 **IDataSource** インターフェイスを実装し、 **IRowset** インターフェイスを組み込む必要があります。

**使用例**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
