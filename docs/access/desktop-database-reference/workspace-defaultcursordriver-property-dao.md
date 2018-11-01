---
title: Workspace.DefaultCursorDriver プロパティ (DAO)
TOCTitle: DefaultCursorDriver Property
ms:assetid: 15a8356d-7ae0-3c8e-fbb7-2d8ad6d9a582
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845499(v=office.15)
ms:contentKeyID: 48543413
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053582
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ce246b7693bdbb0dedc86dcad44dc6c0f6e15638
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872985"
---
# <a name="workspacedefaultcursordriver-property-dao"></a><span data-ttu-id="a60f3-102">Workspace.DefaultCursorDriver プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="a60f3-102">Workspace.DefaultCursorDriver Property (DAO)</span></span>


<span data-ttu-id="a60f3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a60f3-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="syntax"></a><span data-ttu-id="a60f3-104">構文</span><span class="sxs-lookup"><span data-stu-id="a60f3-104">Syntax</span></span>

<span data-ttu-id="a60f3-105">*式*です。DefaultCursorDriver</span><span class="sxs-lookup"><span data-stu-id="a60f3-105">*expression* .DefaultCursorDriver</span></span>

<span data-ttu-id="a60f3-106">\*式\***ワークスペース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a60f3-106">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a60f3-107">注釈</span><span class="sxs-lookup"><span data-stu-id="a60f3-107">Remarks</span></span>

<span data-ttu-id="a60f3-108">設定値または戻り値は、 **[CursorDriverEnum](cursordriverenum-enumeration-dao.md)** クラスの定数のいずれかに設定できます。</span><span class="sxs-lookup"><span data-stu-id="a60f3-108">The setting or return value can be set to one of the **[CursorDriverEnum](cursordriverenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="a60f3-p101">このプロパティの設定値は、プロパティの設定後に確立された接続のみに影響します。 **DefaultCursorDriver** プロパティを変更しても、既存の接続には影響しません。</span><span class="sxs-lookup"><span data-stu-id="a60f3-p101">This property setting only affects connections established after the property has been set. Changing the **DefaultCursorDriver** property has no effect on existing connections.</span></span>

## <a name="example"></a><span data-ttu-id="a60f3-111">例</span><span class="sxs-lookup"><span data-stu-id="a60f3-111">Example</span></span>

<span data-ttu-id="a60f3-p102">次の使用例では、 **NextRecordset** メソッドを使用して、複合 SELECT クエリから返されたデータを表示します。このようなクエリを実行するときは、 **DefaultCursorDriver** プロパティを **dbUseODBCCursor** に設定する必要があります。SELECT ステートメントの一部または全部が 0 件のレコードを返したとしても **NextRecordset** メソッドは **True** を返し、個々の SQL 句をすべて調べた後でのみ **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="a60f3-p102">This example uses the **NextRecordset** method to view the data from a compound SELECT query. The **DefaultCursorDriver** property must be set to **dbUseODBCCursor** when executing such queries. The **NextRecordset** method will return **True** even if some or all of the SELECT statements return zero records; it will return **False** only after all the individual SQL clauses have been checked.</span></span>

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

<span data-ttu-id="a60f3-p103">複合 SQL ステートメントを含むプリペアド ステートメントを作成して、同じ作業を実行することもできます。 **QueryDef** オブジェクトの **CacheSize** プロパティが 1 に設定されていて、 **Recordset** オブジェクトが前方スクロール タイプであり、かつ読み取り専用である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a60f3-p103">Another way to accomplish the same task would be to create a prepared statement containing the compound SQL statement. The **CacheSize** property of the **QueryDef** object must be set to 1, and the **Recordset** object must be forward-only and read-only.</span></span>

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

<br/>

<span data-ttu-id="a60f3-p104">次の使用例は、 **RecordStatus** プロパティおよび **DefaultCursorDriver** プロパティを使用して、バッチ更新中にローカル **Recordset** オブジェクトへの変更が記録される方法を示します。このプロシージャを実行するには、RecordStatusOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="a60f3-p104">This example uses the **RecordStatus** and **DefaultCursorDriver** properties to show how changes to a local **Recordset** are tracked during batch updating. The RecordStatusOutput function is required for this procedure to run.</span></span>

```vb 
Sub RecordStatusX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM authors", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 .MoveFirst 
 Debug.Print "Original record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Edit 
 !au_lname = "Bowen" 
 .Update 
 Debug.Print "Edited record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .AddNew 
 !au_lname = "NewName" 
 .Update 
 Debug.Print "New record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Delete 
 Debug.Print "Deleted record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 ' Close the local recordset without updating the 
 ' data on the server. 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
Function RecordStatusOutput(lngTemp As Long) As String 
 
 Dim strTemp As String 
 
 strTemp = "" 
 
 ' Construct an output string based on the RecordStatus 
 ' value. 
If lngTemp = dbRecordUnmodified Then _ 
 strTemp = "[dbRecordUnmodified]" 
 If lngTemp = dbRecordModified Then _ 
 strTemp = "[dbRecordModified]" 
 If lngTemp = dbRecordNew Then _ 
 strTemp = "[dbRecordNew]" 
 If lngTemp = dbRecordDeleted Then _ 
 strTemp = "[dbRecordDeleted]" 
 If lngTemp = dbRecordDBDeleted Then _ 
 strTemp = "[dbRecordDBDeleted]" 
 
 RecordStatusOutput = strTemp 
 
End Function 
 
```

