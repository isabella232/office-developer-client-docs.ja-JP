---
title: Recordset2.RecordStatus プロパティ (DAO)
TOCTitle: RecordStatus Property
ms:assetid: 178872a9-e361-f277-627d-f91b01ceb6d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845575(v=office.15)
ms:contentKeyID: 48543451
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae3dc5ba640b4b24a7400fc9e467978777ef6fcc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700459"
---
# <a name="recordset2recordstatus-property-dao"></a><span data-ttu-id="a84ab-102">Recordset2.RecordStatus プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="a84ab-102">Recordset2.RecordStatus property (DAO)</span></span>


<span data-ttu-id="a84ab-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a84ab-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="a84ab-104">構文</span><span class="sxs-lookup"><span data-stu-id="a84ab-104">Syntax</span></span>

<span data-ttu-id="a84ab-105">*式*です。RecordStatus</span><span class="sxs-lookup"><span data-stu-id="a84ab-105">*expression* .RecordStatus</span></span>

<span data-ttu-id="a84ab-106">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a84ab-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a84ab-107">注釈</span><span class="sxs-lookup"><span data-stu-id="a84ab-107">Remarks</span></span>

<span data-ttu-id="a84ab-108">**RecordStatus** プロパティの値は、次の共有的バッチ更新でカレント レコードが更新の対象となるかどうかおよびその更新方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a84ab-108">The value of the **RecordStatus** property indicates whether and how the current record will be involved in the next optimistic batch update.</span></span>

<span data-ttu-id="a84ab-p101">ユーザーがレコードを変更すると、そのレコードの **RecordStatus** が自動的に **dbRecordModified** に変更されます。同様に、レコードを追加または削除すると、該当する定数が **RecordStatus** に反映されます。その後、バッチ モード **[Update](recordset2-update-method-dao.md)** メソッドを使用すると、各レコードの **RecordStatus** プロパティに基づいて、DAO が各レコードに対する適切な操作指示をリモート サーバーに送信します。</span><span class="sxs-lookup"><span data-stu-id="a84ab-p101">When a user changes a record, the **RecordStatus** for that record automatically changes to **dbRecordModified**. Similarly, if a record is added or deleted, **RecordStatus** reflects the appropriate constant. When you then use a batch-mode **[Update](recordset2-update-method-dao.md)** method, DAO will submit an appropriate operation to the remote server for each record, based on the record's **RecordStatus** property.</span></span>

## <a name="example"></a><span data-ttu-id="a84ab-112">例</span><span class="sxs-lookup"><span data-stu-id="a84ab-112">Example</span></span>

<span data-ttu-id="a84ab-p102">次の使用例は、 **RecordStatus** プロパティおよび **DefaultCursorDriver** プロパティを使用して、バッチ更新中にローカル **Recordset** オブジェクトへの変更が記録される方法を示します。このプロシージャを実行するには、RecordStatusOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="a84ab-p102">This example uses the **RecordStatus** and **DefaultCursorDriver** properties to show how changes to a local **Recordset** are tracked during batch updating. The RecordStatusOutput function is required for this procedure to run.</span></span>

```vb 
Sub RecordStatusX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
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

