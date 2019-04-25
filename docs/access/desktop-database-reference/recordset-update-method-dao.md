---
title: Recordset.Update メソッド (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 9f73dfc49a6ec99b726a052c588c032783010081
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307526"
---
# <a name="recordsetupdate-method-dao"></a><span data-ttu-id="59fee-102">Recordset.Update メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="59fee-102">Recordset.Update Method (DAO)</span></span>

<span data-ttu-id="59fee-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="59fee-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="59fee-104">構文</span><span class="sxs-lookup"><span data-stu-id="59fee-104">Syntax</span></span>

<span data-ttu-id="59fee-105">*式* .Update(***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="59fee-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="59fee-106">*式* **Recordset** オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="59fee-106">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="59fee-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="59fee-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59fee-108">名前</span><span class="sxs-lookup"><span data-stu-id="59fee-108">Name</span></span></p></th>
<th><p><span data-ttu-id="59fee-109">必須/省略可能</span><span class="sxs-lookup"><span data-stu-id="59fee-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="59fee-110">データ型</span><span class="sxs-lookup"><span data-stu-id="59fee-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="59fee-111">説明</span><span class="sxs-lookup"><span data-stu-id="59fee-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59fee-112"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="59fee-112"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="59fee-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="59fee-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="59fee-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="59fee-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="59fee-115">[設定] で指定されている更新の種類を示す <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> クラスの定数です (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="59fee-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59fee-116"><em>物理的な力</em></span><span class="sxs-lookup"><span data-stu-id="59fee-116"><em>Force</em></span></span></p></td>
<td><p><span data-ttu-id="59fee-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="59fee-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="59fee-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="59fee-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="59fee-p101"><a href="recordset-addnew-method-dao.md"><strong>AddNew</strong></a> 、 <a href="fields-delete-method-dao.md"><strong>Delete</strong></a> 、または <a href="recordset-edit-method-dao.md"><strong>Edit</strong></a> の呼び出し後に、基になるデータが他のユーザーによって変更されたかどうかにかかわらず、変更を強制的にデータベースに反映するかどうかを示すブール型 ( <strong>Boolean</strong> ) の値です。 <strong>True</strong> に設定すると、変更が強制的に反映され、他のユーザーによる変更は単純に上書きされます。 <strong>False</strong> (既定値) に設定すると、更新が保留されている間に他のユーザーが変更を加えた場合、競合する変更の更新が失敗します。エラーは発生しませんが、 <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> プロパティと <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> プロパティに、競合の数と競合によって影響を受ける行が、それぞれ格納されます (ODBCDirect ワークスペースのみ)。  </span><span class="sxs-lookup"><span data-stu-id="59fee-p101">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset-edit-method-dao.md">Edit</a></strong> call. If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten. If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict. No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="59fee-123">注釈</span><span class="sxs-lookup"><span data-stu-id="59fee-123">Remarks</span></span>

<span data-ttu-id="59fee-124">**Update** は、カレント レコードと、それに加えた変更を保存するときに使用します。</span><span class="sxs-lookup"><span data-stu-id="59fee-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59fee-125">[!重要] 次の場合は、カレント レコードに対する変更が失われます。</span><span class="sxs-lookup"><span data-stu-id="59fee-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="59fee-126">**Edit** メソッドまたは **AddNew** メソッドを使用した後、先に **Update** を使用せずに他のレコードに移動した場合。</span><span class="sxs-lookup"><span data-stu-id="59fee-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="59fee-127">**Edit** または **AddNew** を使用した後、先に **Update** を使用せずに、再度 **Edit** または **AddNew** を使用した場合。</span><span class="sxs-lookup"><span data-stu-id="59fee-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="59fee-128">**[Bookmark](recordset-bookmark-property-dao.md)** プロパティを他のレコードに設定した場合。</span><span class="sxs-lookup"><span data-stu-id="59fee-128">You set the **[Bookmark](recordset-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="59fee-129">先に **Update** を使用せずに **Recordset** を閉じた場合。</span><span class="sxs-lookup"><span data-stu-id="59fee-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="59fee-130">[**CancelUpdate**](recordset-cancelupdate-method-dao.md) を使用して **Edit** 操作を取り消した場合。</span><span class="sxs-lookup"><span data-stu-id="59fee-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="59fee-p102">レコードを編集するには、 **Edit** メソッドを使用して、カレント レコードの内容をコピー バッファーにコピーします。先に **Edit** を使用せずに、 **Update** を使用した場合や、フィールドの値を変更しようとした場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="59fee-p102">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer. If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="59fee-133">ODBCDirect ワークスペースでは、カーソル ライブラリが一括更新をサポートしており、 **Recordset** を開くときにオプションとして一括更新時の共有的ロックが指定されている場合に、一括更新を実行できます。</span><span class="sxs-lookup"><span data-stu-id="59fee-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="59fee-134">Microsoft Access ワークスペースでは、マルチユーザー環境で **Recordset** オブジェクトの **LockEdits** プロパティが **True** に設定されている場合 (排他的ロック)、 **Edit** が使用された時点から、 **Update** メソッドが実行されるか、編集が取り消されるまで、レコードがロックされます。</span><span class="sxs-lookup"><span data-stu-id="59fee-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="59fee-135">**LockEdits** プロパティが **False** に設定されている場合 (共有的ロック)、レコードはロックされ、データベースに反映される直前に、編集前のレコードと比較されます。</span><span class="sxs-lookup"><span data-stu-id="59fee-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> 

<span data-ttu-id="59fee-136">**Edit** メソッドを使用した時点からレコードが変更されている場合は、 **Update** 操作が失敗します。</span><span class="sxs-lookup"><span data-stu-id="59fee-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="59fee-137">Microsoft Office Access データベース エンジンに接続されている ODBC データベース、およびインストール可能な ISAM データベースでは、常に共有的ロックが使用されます。</span><span class="sxs-lookup"><span data-stu-id="59fee-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="59fee-138">変更による **Update** 操作を引き続き実行するには、 **Update** メソッドを再度使用します。</span><span class="sxs-lookup"><span data-stu-id="59fee-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="59fee-139">他のユーザーがレコードを変更した後にレコードを戻すには、Move 0 を使用して現在のレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="59fee-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>

> [!NOTE]
> <span data-ttu-id="59fee-p105">レコードを追加、編集、または削除するには、基になるデータ ソースでレコードに一意なインデックスが付けられている必要があります。このようなインデックスがない場合、Microsoft Access ワークスペースで **AddNew**、**Delete**、または **Edit** の各メソッドを呼び出すと、"アクセスが拒否されました。" というエラーが発生し、ODBCDirect ワークスペースで **Update** を呼び出すと、"引数が無効です。" というエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="59fee-p105">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>

## <a name="example"></a><span data-ttu-id="59fee-142">例</span><span class="sxs-lookup"><span data-stu-id="59fee-142">Example</span></span>

<span data-ttu-id="59fee-143">この例では、**Update** メソッドと **Edit** メソッドを組み合わせて使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="59fee-143">This example demonstrates the **Update** method in conjunction with **Edit** method.</span></span>

```vb
    Sub UpdateX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     .Edit 
     ' Store original data. 
     strOldFirst = !FirstName 
     strOldLast = !LastName 
     ' Change data in edit buffer. 
     !FirstName = "Linda" 
     !LastName = "Kobara" 
     
     ' Show contents of buffer and get user input. 
     strMessage = "Edit in progress:" & vbCr & _ 
     " Original data = " & strOldFirst & " " & _ 
     strOldLast & vbCr & " Data in buffer = " & _ 
     !FirstName & " " & !LastName & vbCr & vbCr & _ 
     "Use Update to replace the original data with " & _ 
     "the buffered data in the Recordset?" 
     
     If MsgBox(strMessage, vbYesNo) = vbYes Then 
     .Update 
     Else 
     .CancelUpdate 
     End If 
     
     ' Show the resulting data. 
     MsgBox "Data in recordset = " & !FirstName & " " & _ 
     !LastName 
     
     ' Restore original data because this is a demonstration. 
     If Not (strOldFirst = !FirstName And _ 
     strOldLast = !LastName) Then 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="59fee-144">この例では、 **Update** メソッドと **AddNew** メソッドを組み合わせて使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="59fee-144">This example demonstrates the **Update** method in conjunction with the **AddNew** method.</span></span>

```vb
    Sub UpdateX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     .AddNew 
     !FirstName = "Bill" 
     !LastName = "Sornsin" 
     
     ' Show contents of buffer and get user input. 
     strMessage = "AddNew in progress:" & vbCr & _ 
     " Data in buffer = " & !FirstName & " " & _ 
     !LastName & vbCr & vbCr & _ 
     "Use Update to save buffer to recordset?" 
     
     If MsgBox(strMessage, vbYesNoCancel) = vbYes Then 
     .Update 
     ' Go to the new record and show the resulting data. 
     .Bookmark = .LastModified 
     MsgBox "Data in recordset = " & !FirstName & _ 
     " " & !LastName 
     ' Delete new data because this is a demonstration. 
     .Delete 
     Else 
     .CancelUpdate 
     MsgBox "No new record added." 
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="59fee-145">この例では、 **BatchCollisionCount** プロパティおよび **Update** メソッドを使用して一括更新を実行し、その一括更新ですべての競合を解決する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="59fee-145">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
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
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="59fee-p106">この例では、 **AddNew** メソッドを使用して、指定された名前で新しいレコードを作成します。このプロシージャを実行するには、AddName 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="59fee-p106">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
