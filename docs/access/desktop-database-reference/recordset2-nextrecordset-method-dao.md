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
# <a name="recordset2nextrecordset-method-dao"></a><span data-ttu-id="7b55b-102">NextRecordset メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="7b55b-102">Recordset2.NextRecordset method (DAO)</span></span>


<span data-ttu-id="7b55b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b55b-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="7b55b-104">構文</span><span class="sxs-lookup"><span data-stu-id="7b55b-104">Syntax</span></span>

<span data-ttu-id="7b55b-105">*式*。NextRecordset</span><span class="sxs-lookup"><span data-stu-id="7b55b-105">*expression* .NextRecordset</span></span>

<span data-ttu-id="7b55b-106">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="7b55b-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b55b-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b55b-107">Return value</span></span>

<span data-ttu-id="7b55b-108">Boolean</span><span class="sxs-lookup"><span data-stu-id="7b55b-108">Boolean</span></span>

## <a name="remarks"></a><span data-ttu-id="7b55b-109">注釈</span><span class="sxs-lookup"><span data-stu-id="7b55b-109">Remarks</span></span>

<span data-ttu-id="7b55b-110">ODBCDirect ワークスペースでは、次の例に示すように、 **OpenRecordset**の source 引数に複数の選択クエリを含む**Recordset** 、または select クエリ**[QueryDef](querydef-object-dao.md)** オブジェクトの**[SQL](querydef-sql-property-dao.md)** プロパティを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="7b55b-110">In an ODBCDirect workspace, you can open a **Recordset** containing more than one select query in the source argument of **OpenRecordset**, or the **[SQL](querydef-sql-property-dao.md)** property of a select query **[QueryDef](querydef-object-dao.md)** object, as in the following example.</span></span>

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

<span data-ttu-id="7b55b-p101">返される **Recordset** では、最初のクエリの結果が表示されます。それ以降のクエリの結果であるレコードのセットを取得するには、 **NextRecordset** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="7b55b-p101">The returned **Recordset** will open with the results of the first query. To obtain the result sets of records from subsequent queries, use the **NextRecordset** method.</span></span>

<span data-ttu-id="7b55b-p102">取得できるレコードがさらに存在する (つまり **OpenRecordset** への呼び出しまたは **SQL** プロパティで指定されている選択クエリが他にもある) 場合、次のクエリから返されるレコードが **Recordset** に読み込まれ、 **NextRecordset** は **True** を返します。これは、レコードが取得できる状態であることを示します。取得できるレコードがない (つまり最後の選択クエリの結果が既に **Recordset** に読み込まれている) 場合、 **NextRecordset** は **False** を返し、 **Recordset** は空になります。</span><span class="sxs-lookup"><span data-stu-id="7b55b-p102">If more records are available (that is, there was another select query in the **OpenRecordset** call or in the **SQL** property), the records returned from the next query will be loaded into the **Recordset**, and **NextRecordset** will return **True**, indicating that the records are available. When no more records are available (that is, results of the last select query have been loaded into the **Recordset**), then **NextRecordset** will return **False**, and the **Recordset** will be empty.</span></span>

<span data-ttu-id="7b55b-p103">**[Cancel](connection-cancel-method-dao.md)** メソッドを使用して、 **Recordset** の内容を消去することもできます。ただし、 **Cancel** を使用すると、まだ読み込まれていないレコードも消去されます。</span><span class="sxs-lookup"><span data-stu-id="7b55b-p103">You can also use the **[Cancel](connection-cancel-method-dao.md)** method to flush the contents of a **Recordset**. However, **Cancel** also flushes any additional records not yet loaded.</span></span>

## <a name="example"></a><span data-ttu-id="7b55b-117">例</span><span class="sxs-lookup"><span data-stu-id="7b55b-117">Example</span></span>

<span data-ttu-id="7b55b-p104">次の使用例は、 **NextRecordset** メソッドを使用して、複合 SELECT クエリからのデータを表示します。このようなクエリを実行する場合、 **DefaultCursorDriver** プロパティを **dbUseODBCCursor** に設定する必要があります。 **NextRecordset** メソッドは、一部またはすべての SELECT ステートメントが 0 件のレコードを返す場合でも **True** を返し、 **False** を返すのは、個別の SQL 句をすべて確認した後のみです。</span><span class="sxs-lookup"><span data-stu-id="7b55b-p104">This example uses the **NextRecordset** method to view the data from a compound SELECT query. The **DefaultCursorDriver** property must be set to **dbUseODBCCursor** when executing such queries. The **NextRecordset** method will return **True** even if some or all of the SELECT statements return zero records; it will return **False** only after all the individual SQL clauses have been checked.</span></span>

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

<span data-ttu-id="7b55b-p105">同じ処理を実行するための別の方法として、複合 SQL ステートメントを含むステートメントをあらかじめ作成しておく方法があります。この場合は、 **QueryDef** オブジェクトの **CacheSize** プロパティを 1 に設定し、 **Recordset** オブジェクトを読み取り専用の前方スクロール タイプとする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b55b-p105">Another way to accomplish the same task would be to create a prepared statement containing the compound SQL statement. The **CacheSize** property of the **QueryDef** object must be set to 1, and the **Recordset** object must be forward-only and read-only.</span></span>

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

