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
localization_priority: Normal
ms.openlocfilehash: 5950154d8896678889af01254104a2ac0dfef4cc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712435"
---
# <a name="recordsetcancelupdate-method-dao"></a>Recordset.CancelUpdate メソッド (DAO)

**適用されます**Access 2013、Office 2013。

**[Recordset](recordset-object-dao.md)** オブジェクトで保留中のすべての更新を取り消します。

## <a name="syntax"></a>構文

*式*です。CancelUpdate (***UpdateType***)

*式***レコード セット**オブジェクトを表す変数です。

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
<td><p><strong>Long</strong></p></td>
<td><p><strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong>値のいずれかに設定します。</p><p><strong>注</strong>: <EM>dbUpdateRegular</EM>および<EM>dbUpdateBatch</EM>値は、バッチ更新が有効になっている場合にのみ有効です。</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**CancelUpdate** メソッドを使用すると、 **[Edit](recordset-edit-method-dao.md)** メソッドまたは **[AddNew](recordset-addnew-method-dao.md)** メソッドの操作によるすべての保留中の更新を取り消すことができます。たとえば、ユーザーが **Edit** メソッドまたは **AddNew** メソッドを呼び出し、 **Update** メソッドを呼び出していない場合に **CancelUpdate** を使用すると、 **Edit** メソッドまたは **AddNew** メソッドを呼び出してから行われたすべての変更を取り消すことができます。

[Recordset](recordset-editmode-property-dao.md) の ****EditMode**** プロパティを確認して、取り消すことができる保留中の操作があるかどうかを確認します。

> [!NOTE]
> [!メモ] **CancelUpdate** メソッドを使用することは、カレント レコードが変更されないこと、 **[BOF](recordset-update-method-dao.md)** 、 **[EOF](recordset-bof-property-dao.md)** などの各種のプロパティが更新されないことを除いて、 **[Update](recordset-eof-property-dao.md)** メソッドを使用せずに別のレコードに移動することと同じです。


## <a name="example"></a>例

この例では、 **CancelUpdate** メソッドを **AddNew** メソッドと共に使用する方法を示します。

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

