---
title: Recordset.Update メソッド (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 48ab6c6c2aa61fbfda52b60c88dfd301742aaf87
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891087"
---
# <a name="recordsetupdate-method-dao"></a>Recordset.Update メソッド (DAO)

**適用されます**Access 2013、Office 2013。

## <a name="syntax"></a>構文

*式*です。更新 (***UpdateType***、***力***)

*式***レコード セット**オブジェクトを表す変数です。

### <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>UpdateType</p></td>
<td><p>省略可能</p></td>
<td><p><strong>長整数型 (Long)</strong></p></td>
<td><p>[設定] で指定されている更新の種類を示す <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> クラスの定数です (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p>Force</p></td>
<td><p>省略可能</p></td>
<td><p><strong>ブール型 (Boolean)</strong></p></td>
<td><p><a href="recordset-addnew-method-dao.md"><strong>AddNew</strong></a> 、 <a href="fields-delete-method-dao.md"><strong>Delete</strong></a> 、または <a href="recordset-edit-method-dao.md"><strong>Edit</strong></a> の呼び出し後に、基になるデータが他のユーザーによって変更されたかどうかにかかわらず、変更を強制的にデータベースに反映するかどうかを示すブール型 ( <strong>Boolean</strong> ) の値です。 <strong>True</strong> に設定すると、変更が強制的に反映され、他のユーザーによる変更は単純に上書きされます。 <strong>False</strong> (既定値) に設定すると、更新が保留されている間に他のユーザーが変更を加えた場合、競合する変更の更新が失敗します。エラーは発生しませんが、 <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> プロパティと <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> プロパティに、競合の数と競合によって影響を受ける行が、それぞれ格納されます (ODBCDirect ワークスペースのみ)。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**Update** は、カレント レコードと、それに加えた変更を保存するために使用します。

> [!IMPORTANT]
> [!重要] 次の場合は、カレント レコードに対する変更が失われます。
> - **Edit** メソッドまたは **AddNew** メソッドを使用した後、先に **Update** を使用せずに他のレコードに移動した場合。
> - **Edit** または **AddNew** を使用した後、先に **Update** を使用せずに、再度 **Edit** または **AddNew** を使用した場合。
> - **[Bookmark](recordset-bookmark-property-dao.md)** プロパティを他のレコードに設定した場合。
> - 先に **Update** を使用せずに **Recordset** を閉じた場合。
> - [**CancelUpdate**](recordset-cancelupdate-method-dao.md) を使用して **Edit** 操作を取り消した場合。

レコードを編集するには、 **Edit** メソッドを使用して、カレント レコードの内容をコピー バッファーにコピーします。先に **Edit** を使用せずに、 **Update** を使用した場合や、フィールドの値を変更しようとした場合は、エラーが発生します。

ODBCDirect ワークスペースでは、カーソル ライブラリが一括更新をサポートしており、 **Recordset** を開くときにオプションとして一括更新時の共有的ロックが指定されている場合に、一括更新を実行できます。

Microsoft Access ワークスペースでは、マルチユーザー環境で **Recordset** オブジェクトの **LockEdits** プロパティが **True** に設定されている場合 (排他的ロック)、 **Edit** が使用された時点から、 **Update** メソッドが実行されるか、編集が取り消されるまで、レコードがロックされます。 **LockEdits** プロパティが **False** に設定されている場合 (共有的ロック)、レコードはロックされ、データベースに反映される直前に、編集前のレコードと比較されます。 

**Edit** メソッドを使用した時点からレコードが変更されている場合は、 **Update** 操作が失敗します。 Microsoft Office Access データベース エンジンに接続されている ODBC データベース、およびインストール可能な ISAM データベースでは、常に共有的ロックが使用されます。 変更による **Update** 操作を引き続き実行するには、 **Update** メソッドを再度使用します。 変更を他のユーザーのレコードを元に戻す、Move 0 を使用して現在のレコードを更新します。


> [!NOTE]
> [!メモ] レコードを追加、編集、または削除するには、基になるデータ ソースでレコードに一意なインデックスが付けられている必要があります。このようなインデックスがない場合、Microsoft Access ワークスペースで **AddNew** 、 **Delete** 、または **Edit** の各メソッドを呼び出すと、"アクセスが拒否されました。" というエラーが発生し、ODBCDirect ワークスペースで **Update** を呼び出すと、"引数が無効です。" というエラーが発生します。

## <a name="example"></a>例

この例では、 **Update** メソッドと **Edit** メソッドを組み合わせて使用する方法を示します。

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

この例では、 **Update** メソッドと **AddNew** メソッドを組み合わせて使用する方法を示します。

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

この例では、 **BatchCollisionCount** プロパティおよび **Update** メソッドを使用して一括更新を実行し、その一括更新ですべての競合を解決する方法を示します。

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

この例では、 **AddNew** メソッドを使用して、指定された名前で新しいレコードを作成します。このプロシージャを実行するには、AddName 関数が必要です。

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
