---
title: NextRecordset メソッド (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 33288131-d4f3-0159-1736-f401346087f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192318(v=office.15)
ms:contentKeyID: 48544096
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053575
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 54d0e49dfbe9dc3fb87eb10af9eefe3aa2f83709
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307239"
---
# <a name="recordset2nextrecordset-method-dao"></a>NextRecordset メソッド (DAO)


**適用先:** Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*。NextRecordset

*式***Recordset2**オブジェクトを表す変数を取得します。

## <a name="return-value"></a>戻り値

Boolean

## <a name="remarks"></a>注釈

ODBCDirect ワークスペースでは、次の例に示すように、 **OpenRecordset**の source 引数に複数の選択クエリを含む**Recordset** 、または select クエリ**[QueryDef](querydef-object-dao.md)** オブジェクトの**[SQL](querydef-sql-property-dao.md)** プロパティを開くことができます。

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

返される **Recordset** では、最初のクエリの結果が表示されます。それ以降のクエリの結果であるレコードのセットを取得するには、 **NextRecordset** メソッドを使用します。

取得できるレコードがさらに存在する (つまり **OpenRecordset** への呼び出しまたは **SQL** プロパティで指定されている選択クエリが他にもある) 場合、次のクエリから返されるレコードが **Recordset** に読み込まれ、 **NextRecordset** は **True** を返します。これは、レコードが取得できる状態であることを示します。取得できるレコードがない (つまり最後の選択クエリの結果が既に **Recordset** に読み込まれている) 場合、 **NextRecordset** は **False** を返し、 **Recordset** は空になります。

**[Cancel](connection-cancel-method-dao.md)** メソッドを使用して、 **Recordset** の内容を消去することもできます。ただし、 **Cancel** を使用すると、まだ読み込まれていないレコードも消去されます。

## <a name="example"></a>例

次の使用例は、 **NextRecordset** メソッドを使用して、複合 SELECT クエリからのデータを表示します。このようなクエリを実行する場合、 **DefaultCursorDriver** プロパティを **dbUseODBCCursor** に設定する必要があります。 **NextRecordset** メソッドは、一部またはすべての SELECT ステートメントが 0 件のレコードを返す場合でも **True** を返し、 **False** を返すのは、個別の SQL 句をすべて確認した後のみです。

```vb
    Sub NextRecordsetX() 
     
     Dim wrkODBC As Workspace 
     Dim conPubs As Connection 
     Dim rstTemp As Recordset2 
     Dim intCount As Integer 
     Dim booNext As Boolean 
     
     ' Create ODBCDirect Workspace object and open Connection 
     ' object. The DefaultCursorDriver setting is required 
     ' when using compound SQL statements. 
     Set wrkODBC = CreateWorkspace("", _ 
     "admin", "", dbUseODBC) 
     wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
     
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Construct compound SELECT statement. 
     Set rstTemp = conPubs.OpenRecordset("SELECT * " & _ 
     "FROM authors; " & _ 
     "SELECT * FROM stores; " & _ 
     "SELECT * FROM jobs") 
     
     ' Try printing results from each of the three SELECT 
     ' statements. 
     booNext = True 
     intCount = 1 
     With rstTemp 
     Do While booNext 
     Debug.Print "Contents of recordset #" & intCount 
     Do While Not .EOF 
     Debug.Print , .Fields(0), .Fields(1) 
     .MoveNext 
     Loop 
     booNext = .NextRecordset 
     Debug.Print " rstTemp.NextRecordset = " & _ 
     booNext 
     intCount = intCount + 1 
     Loop 
     End With 
     
     rstTemp.Close 
     conPubs.Close 
     wrkODBC.Close 
     
    End Sub 
```

<br/>

同じ処理を実行するための別の方法として、複合 SQL ステートメントを含むステートメントをあらかじめ作成しておく方法があります。この場合は、 **QueryDef** オブジェクトの **CacheSize** プロパティを 1 に設定し、 **Recordset** オブジェクトを読み取り専用の前方スクロール タイプとする必要があります。

```vb 
Sub NextRecordsetX2() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset2 
 Dim intCount As Integer 
 Dim booNext As Boolean 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. The DefaultCursorDriver setting is required 
 ' when using compound SQL statements. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Create a temporary stored procedure with a compound 
 ' SELECT statement. 
 Set qdfTemp = conPubs.CreateQueryDef("", _ 
 "SELECT * FROM authors; " & _ 
 "SELECT * FROM stores; " & _ 
 "SELECT * FROM jobs") 
 ' Set CacheSize and open Recordset object with arguments 
 ' that will allow access to multiple recordsets. 
 qdfTemp.CacheSize = 1 
 Set rstTemp = qdfTemp.OpenRecordset(dbOpenForwardOnly, _ 
 dbReadOnly) 
 
 ' Try printing results from each of the three SELECT 
 ' statements. 
 booNext = True 
 intCount = 1 
 With rstTemp 
 Do While booNext 
 Debug.Print "Contents of recordset #" & intCount 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 booNext = .NextRecordset 
 Debug.Print " rstTemp.NextRecordset = " & _ 
 booNext 
 intCount = intCount + 1 
 Loop 
 End With 
 
 rstTemp.Close 
 qdfTemp.Close 
 conPubs.Close 
 wrkODBC.Close 
 
End Sub 
 
```

