---
title: Recordset2.CancelUpdate メソッド (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: f741dec1-b9a4-506e-74ec-2bc309b0918e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836907(v=office.15)
ms:contentKeyID: 48548761
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9679a39a8509bb73e9d788e776e208f3c899d3c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998407"
---
# <a name="recordset2cancelupdate-method-dao"></a>Recordset2.CancelUpdate メソッド (DAO)

**適用されます**Access 2013、Office 2013。

**[Recordset](recordset-object-dao.md)** オブジェクトで保留中のすべての更新を取り消します。

## <a name="syntax"></a>構文

*式*です。CancelUpdate (***UpdateType***)

*式***Recordset2**オブジェクトを表す変数です。

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
<td><p><em>UpdateType</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>長整数型 (Long)</strong></p></td>
<td><p><strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong>値のいずれかに設定します。</p><p><strong>注</strong>: <EM>dbUpdateRegular</EM>および<EM>dbUpdateBatch</EM>値は、バッチ更新が有効になっている場合にのみ有効です。</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**CancelUpdate** メソッドを使用すると、 **[Edit](recordset2-edit-method-dao.md)** メソッドまたは **[AddNew](recordset2-addnew-method-dao.md)** メソッドの操作によるすべての保留中の更新を取り消すことができます。たとえば、ユーザーが **Edit** メソッドまたは **AddNew** メソッドを呼び出し、 **Update** メソッドを呼び出していない場合に **CancelUpdate** を使用すると、 **Edit** メソッドまたは **AddNew** メソッドを呼び出してから行われたすべての変更を取り消すことができます。

[Recordset](recordset2-editmode-property-dao.md) の ****EditMode**** プロパティを確認して、取り消すことができる保留中の操作があるかどうかを確認します。

> [!NOTE]
> [!メモ] **CancelUpdate** メソッドを使用することは、カレント レコードが変更されないこと、 **[BOF](recordset2-update-method-dao.md)** 、 **[EOF](recordset2-bof-property-dao.md)** などの各種のプロパティが更新されないことを除いて、 **[Update](recordset2-eof-property-dao.md)** メソッドを使用せずに別のレコードに移動することと同じです。

## <a name="example"></a>例

この例では、 **CancelUpdate** メソッドを **AddNew** メソッドと共に使用する方法を示します。

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

この例では、 **CancelUpdate** メソッドを **Edit** メソッドと共に使用する方法を示します。

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

