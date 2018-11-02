---
title: Recordset.NextRecordset メソッド (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 4a3a6176-0aa0-efb6-b175-dbe23e266abc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193483(v=office.15)
ms:contentKeyID: 48544664
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4a6cf889e7676895534b053e8aacd4bb0eada89
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919354"
---
# <a name="recordsetnextrecordset-method-dao"></a><span data-ttu-id="3b569-102">Recordset.NextRecordset メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="3b569-102">Recordset.NextRecordset method (DAO)</span></span>


<span data-ttu-id="3b569-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3b569-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="3b569-104">構文</span><span class="sxs-lookup"><span data-stu-id="3b569-104">Syntax</span></span>

<span data-ttu-id="3b569-105">*式*です。NextRecordset</span><span class="sxs-lookup"><span data-stu-id="3b569-105">*expression* .NextRecordset</span></span>

<span data-ttu-id="3b569-106">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="3b569-106">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="return-value"></a><span data-ttu-id="3b569-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="3b569-107">Return value</span></span>

<span data-ttu-id="3b569-108">ブール型</span><span class="sxs-lookup"><span data-stu-id="3b569-108">Boolean</span></span>

## <a name="remarks"></a><span data-ttu-id="3b569-109">注釈</span><span class="sxs-lookup"><span data-stu-id="3b569-109">Remarks</span></span>

<span data-ttu-id="3b569-110">ODBCDirect ワークスペースでは、内の**何らか**の場合は、変換元の引数または**[クエリ定義](querydef-object-dao.md)** オブジェクトは、次の例のように選択クエリの**[SQL](querydef-sql-property-dao.md)** プロパティに 1 つ以上の select クエリが含まれている**[レコード セット](recordset-object-dao.md)** を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="3b569-110">In an ODBCDirect workspace, you can open a **[Recordset](recordset-object-dao.md)** containing more than one select query in the source argument of **OpenRecordset**, or the **[SQL](querydef-sql-property-dao.md)** property of a select query **[QueryDef](querydef-object-dao.md)** object, as in the following example.</span></span>

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

<span data-ttu-id="3b569-p101">返される **Recordset** は、最初のクエリの結果に基づいて開かれます。次のクエリの結果に基づくレコードの結果セットを取得するには、 **NextRecordset** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3b569-p101">The returned **Recordset** will open with the results of the first query. To obtain the result sets of records from subsequent queries, use the **NextRecordset** method.</span></span>

<span data-ttu-id="3b569-p102">他にもレコードがある (つまり、 **OpenRecordset** 呼び出しまたは **SQL** プロパティに別の選択クエリが指定されていた) 場合は、次のクエリから返されるレコードが **Recordset** に読み込まれ、 **NextRecordset** はレコードがあることを示す **True** を返します。これ以上レコードがない (つまり、最後の選択クエリの結果が既に **Recordset** に読み込まれていた) 場合は、 **NextRecordset** は **False** を返し、 **Recordset** は空になります。</span><span class="sxs-lookup"><span data-stu-id="3b569-p102">If more records are available (that is, there was another select query in the **OpenRecordset** call or in the **SQL** property), the records returned from the next query will be loaded into the **Recordset**, and **NextRecordset** will return **True**, indicating that the records are available. When no more records are available (that is, results of the last select query have been loaded into the **Recordset**), then **NextRecordset** will return **False**, and the **Recordset** will be empty.</span></span>

<span data-ttu-id="3b569-p103">**[Cancel](connection-cancel-method-dao.md)** メソッドを使用して、 **Recordset** の内容を消去することもできます。ただし、 **Cancel** を使用すると、まだ読み込まれていないレコードも消去されます。</span><span class="sxs-lookup"><span data-stu-id="3b569-p103">You can also use the **[Cancel](connection-cancel-method-dao.md)** method to flush the contents of a **Recordset**. However, **Cancel** also flushes any additional records not yet loaded.</span></span>

## <a name="example"></a><span data-ttu-id="3b569-117">例</span><span class="sxs-lookup"><span data-stu-id="3b569-117">Example</span></span>

<span data-ttu-id="3b569-p104">次の使用例では、 **NextRecordset** メソッドを使用して、複合 SELECT クエリから返されたデータを表示します。このようなクエリを実行するときは、 **DefaultCursorDriver** プロパティを **dbUseODBCCursor** に設定する必要があります。SELECT ステートメントの一部または全部が 0 件のレコードを返したとしても **NextRecordset** メソッドは **True** を返し、個々の SQL 句をすべて調べた後でのみ **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="3b569-p104">This example uses the **NextRecordset** method to view the data from a compound SELECT query. The **DefaultCursorDriver** property must be set to **dbUseODBCCursor** when executing such queries. The **NextRecordset** method will return **True** even if some or all of the SELECT statements return zero records; it will return **False** only after all the individual SQL clauses have been checked.</span></span>

```vb
    Sub NextRecordsetX() 
     
     Dim wrkODBC As Workspace 
     Dim conPubs As Connection 
     Dim rstTemp As Recordset 
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

<span data-ttu-id="3b569-p105">複合 SQL ステートメントを含むプリペアド ステートメントを作成して、同じ作業を実行することもできます。 **QueryDef** オブジェクトの **CacheSize** プロパティが 1 に設定されていて、 **Recordset** オブジェクトが前方スクロール タイプであり、かつ読み取り専用である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b569-p105">Another way to accomplish the same task would be to create a prepared statement containing the compound SQL statement. The **CacheSize** property of the **QueryDef** object must be set to 1, and the **Recordset** object must be forward-only and read-only.</span></span>

```vb 
Sub NextRecordsetX2() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
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

