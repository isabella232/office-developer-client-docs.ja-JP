---
title: Recordset.CancelUpdate メソッド (DAO)
TOCTitle: CancelUpdate method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: fa3b54650967dd2fef435374b8b6eace327df3dd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593741"
---
# <a name="recordsetcancelupdate-method-dao"></a>Recordset.CancelUpdate メソッド (DAO)

**適用先**: Access 2013、Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクトで、保留中のすべての更新をキャンセルします。

## <a name="syntax"></a>構文

*式* .CancelUpdate(***UpdateType***)

*expression*: **Recordset** オブジェクトを表す変数。

## <a name="parameters"></a>パラメーター

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
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>UpdateType</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Long</strong></p></td>
<td><p><strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum のいずれかの値に設定</a></strong>します。</p><p><strong>注</strong>: <EM>dbUpdateRegular および</EM> <EM>dbUpdateBatch</EM> の値は、バッチ更新が有効になっている場合にのみ有効です。</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**CancelUpdate** メソッドを使用すると、 **[Edit](recordset-edit-method-dao.md)** または **[AddNew](recordset-addnew-method-dao.md)** のいずれかの操作によって生じた保留中の更新を取り消すこどができます。たとえば、 **Edit** メソッドまたは **AddNew** メソッドが呼び出されたが、 **Update** メソッドはまだ呼び出されていない場合、 **CancelUpdate** を使用すると、 **Edit** または **AddNew** の呼び出し後に加えられた変更が取り消されます。

Recordset の **[EditMode](recordset-editmode-property-dao.md)** プロパティ **を** 確認して、取り消し可能な保留中の操作があるかどうかを確認します。

> [!NOTE]
> [!メモ] **CancelUpdate** メソッドを使用すると、 **[Update](recordset-update-method-dao.md)** メソッドを使用せずに他のレコードへ移動するのと同じ効果が得られます。ただし、カレント レコードは変化せず、 **[BOF](recordset-bof-property-dao.md)** プロパティや **[EOF](recordset-eof-property-dao.md)** プロパティなどのさまざまなプロパティは更新されません。


## <a name="example"></a>例

次の例では、 **CancelUpdate** メソッドを **AddNew** メソッドと共に使用する方法を示します。

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "Employees", dbOpenDynaset) 
     
       With rstEmployees 
          .AddNew 
          !FirstName = "Kimberly" 
          !LastName = "Bowen" 
          intCommand = MsgBox("Add new record for " & _ 
             !FirstName & " " & !LastName & "?", vbYesNo) 
          If intCommand = vbYes Then 
             .Update 
             MsgBox "Record added." 
             ' Delete new record because this is a  
             ' demonstration. 
             .Bookmark = .LastModified 
             .Delete 
          Else 
             .CancelUpdate 
             MsgBox "Record not added." 
          End If 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

次の例では、 **CancelUpdate** メソッドを **Edit** メソッドと共に使用する方法を示します。

```vb
Sub CancelUpdateX2() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim strFirst As String 
   Dim strLast As String 
   Dim intCommand As Integer 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
      "Employees", dbOpenDynaset) 
 
   With rstEmployees 
      strFirst = !FirstName 
      strLast = !LastName 
      .Edit 
      !FirstName = "Cora" 
      !LastName = "Edmonds" 
      intCommand = MsgBox("Replace current name with " & _ 
         !FirstName & " " & !LastName & "?", vbYesNo) 
      If intCommand = vbYes Then 
         .Update 
         MsgBox "Record modified." 
         ' Restore data because this is a demonstration. 
         .Bookmark = .LastModified 
         .Edit 
         !FirstName = strFirst 
         !LastName = strLast 
         .Update 
      Else 
         .CancelUpdate 
         MsgBox "Record not modified." 
      End If 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
 
```

