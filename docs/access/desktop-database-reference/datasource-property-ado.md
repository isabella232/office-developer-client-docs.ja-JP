---
title: DataSource プロパティ (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a6b889deb9ccf713c2313b207387be8f6b1681b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868162"
---
# <a name="datasource-property-ado"></a>DataSource プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) オブジェクトとして表されるデータを持つオブジェクトを示します。

## <a name="remarks"></a>解説

データ環境でのデータ バインド コントロールを作成するのにはこのプロパティを使用します。 *.* の**Recordset**オブジェクトとして表されるオブジェクト (*データ メンバー*) の名前を格納しているデータ (データ ソース) のコレクションを管理します。

[DataMember](datamember-property-ado.md) プロパティと **DataSource** プロパティは組み合わせて使用する必要があります。

参照されるオブジェクトには、 **IDataSource** インターフェイスを実装し、 **IRowset** インターフェイスを組み込む必要があります。

**使用例**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
