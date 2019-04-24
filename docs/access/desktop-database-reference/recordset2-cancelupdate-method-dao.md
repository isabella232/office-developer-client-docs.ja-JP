---
title: Recordset2 メソッド (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: f741dec1-b9a4-506e-74ec-2bc309b0918e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836907(v=office.15)
ms:contentKeyID: 48548761
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 90378dc61d12485a290bbd7857d026a46cd9da96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307400"
---
# <a name="recordset2cancelupdate-method-dao"></a>Recordset2 メソッド (DAO)

**適用先:** Access 2013、Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクトの保留中の更新をキャンセルします。

## <a name="syntax"></a>構文

*式*。CancelUpdate (***updatetype***)

*式***Recordset2**オブジェクトを表す変数を取得します。

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
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>updatetype</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>長整数型 (Long)</strong></p></td>
<td><p><strong><a href="updatetypeenum-enumeration-dao.md">updatetypeenum</a></strong>値の1つに設定します。</p><p><strong>注</strong>: <EM>dbUpdateRegular</EM>および<EM>dbUpdateBatch</EM>の値は、バッチ更新が有効になっている場合にのみ有効です。</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**CancelUpdate** メソッドを使用すると、 **[Edit](recordset2-edit-method-dao.md)** または **[AddNew](recordset2-addnew-method-dao.md)** のいずれかの操作によって生じた保留中の更新を取り消すこどができます。たとえば、 **Edit** メソッドまたは **AddNew** メソッドが呼び出されたが、 **Update** メソッドはまだ呼び出されていない場合、 **CancelUpdate** を使用すると、 **Edit** または **AddNew** の呼び出し後に加えられた変更が取り消されます。

**Recordset**の**[EditMode](recordset2-editmode-property-dao.md)** プロパティを調べて、取り消すことができる保留中の操作があるかどうかを確認します。

> [!NOTE]
> [!メモ] **CancelUpdate** メソッドを使用すると、 **[Update](recordset2-update-method-dao.md)** メソッドを使用せずに他のレコードへ移動するのと同じ効果が得られます。ただし、カレント レコードは変化せず、 **[BOF](recordset2-bof-property-dao.md)** プロパティや **[EOF](recordset2-eof-property-dao.md)** プロパティなどのさまざまなプロパティは更新されません。

## <a name="example"></a>例

次の例では、 **CancelUpdate** メソッドを **AddNew** メソッドと共に使用する方法を示します。

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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

