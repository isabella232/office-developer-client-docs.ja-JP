---
title: QueryDef.ODBCTimeout プロパティ (DAO)
TOCTitle: ODBCTimeout Property
ms:assetid: b251c4fb-64a8-aa95-deed-64425df3e00c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822019(v=office.15)
ms:contentKeyID: 48547166
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053052
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: a79f403d49db1137d8b67d2dc7fb27b3ea140fc3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589240"
---
# <a name="querydefodbctimeout-property-dao"></a>QueryDef.ODBCTimeout プロパティ (DAO)


**適用先**: Access 2013、Office 2013

ODBC データベースに対して **[QueryDef](querydef-object-dao.md)** を実行したときに、タイムアウト エラーが発生するまでの待ち時間を秒単位で示します。

## <a name="syntax"></a>構文

*式* .ODBCTimeout

*式* **QueryDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**ODBCTimeout** プロパティを -1 に設定すると、既定では **、QueryDef** を含む **[Connection](connection-object-dao.md)** オブジェクトまたは **[Database](database-object-dao.md)** オブジェクトの **[QueryTimeout](database-querytimeout-property-dao.md)** プロパティの現在の設定がタイムアウトになります。 **ODBCTimeout** プロパティを 0 に設定すると、タイムアウト エラーは発生しません。

Microsoft SQL Server などの ODBC データベースを使用している場合、ネットワーク トラフィックや ODBC サーバーに対する負荷の増大のために、遅延が発生することがあります。無限に待機しないように、エラーが返されるまでの待ち時間を指定できます。

**QueryDef** オブジェクトの **ODBCTimeout** プロパティの設定値は、 **QueryDef** オブジェクトに含まれている **Connection** オブジェクトまたは **Database** オブジェクトの **QueryTimeout** プロパティで指定される値より優先されますが、これはその **QueryDef** オブジェクトに対してのみ有効です。

## <a name="example"></a>例

この例では、**ODBCTimeout** プロパティおよび **QueryTimeout** プロパティを使用して、**Database** オブジェクトの **QueryTimeout** プロパティで、**Database** オブジェクトから作成された **QueryDef** オブジェクトの **ODBCTimeout** プロパティの既定値を設定する方法を示します。

```vb 
Sub ODBCTimeoutX() 
 
 Dim dbsCurrent As Database 
 Dim qdfStores As QueryDef 
 Dim rstStores As Recordset 
 
 Set dbsCurrent = OpenDatabase("Northwind.mdb") 
 
 ' Change the default QueryTimeout of the Northwind 
 ' database. 
 Debug.Print "Default QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 dbsCurrent.QueryTimeout = 30 
 Debug.Print "New QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 
 ' Create a new QueryDef object. 
 Set qdfStores = dbsCurrent.CreateQueryDef("Stores", _ 
 "SELECT * FROM stores") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the SQL Server. 
 qdfStores.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 
 ' Change the ODBCTimeout setting of the new QueryDef 
 ' object from its default setting. 
 Debug.Print "Default ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 qdfStores.ODBCTimeout = 0 
 Debug.Print "New ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 
 ' Execute the query and display the results. 
 Set rstStores = qdfStores.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstStores 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfStores.Name 
 dbsCurrent.Close 
 
End Sub 
 
```

