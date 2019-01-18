---
title: Recordset2.Move メソッド (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d57e73c52ca515f13d613ed3aeb9cf361054396e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707116"
---
# <a name="recordset2move-method-dao"></a>Recordset2.Move メソッド (DAO)

**適用されます**Access 2013、Office 2013。

**[Recordset](recordset-object-dao.md)** オブジェクトでカレント レコードの位置を移動します。

## <a name="syntax"></a>構文

*式*です。移動 (***行***、 ***StartBookmark***)

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
<td><p><em>Rows</em></p></td>
<td><p>必須</p></td>
<td><p><strong>長整数型 (Long)</strong></p></td>
<td><p>位置を移動する行数。rows が 0 より大きい場合は、前方 (ファイルの末尾) に向かって位置が移動します。rows が 0 より小さい場合は、後方 (ファイルの先頭) に向かって位置が移動します。</p></td>
</tr>
<tr class="even">
<td><p><em>StartBookmark</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>ブックマークを示す値。startbookmark を指定した場合、このブックマークが移動の開始位置となります。それ以外の場合は、カレント レコードが移動の開始位置となります。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**Move** を使用して、カレント レコード ポインターの位置を最初のレコードより前に移動しようとすると、カレント レコード ポインターはファイルの先頭に移動します。 **Recordset** 内にレコードがなく、かつ **[BOF](recordset2-bof-property-dao.md)** プロパティが **True** の場合、このメソッドを使用して後方に向かって移動すると、エラーが発生します。

**Move** を使用して、カレント レコード ポインターの位置を最後のレコードよりも後に移動しようとすると、カレント レコード ポインターはファイルの末尾に移動します。 **Recordset** 内にレコードがなく、かつ **[EOF](recordset2-eof-property-dao.md)** プロパティが **True** の場合、このメソッドを使用して前方に向かって移動しようとすると、エラーが発生します。

**BOF** プロパティまたは **EOF** プロパティが **True** の場合に、有効なブックマークを指定せずに **Move** メソッドを使用しようとすると、実行時エラーが発生します。

> [!NOTE]
> - 前方スクロール タイプの **Recordset** オブジェクトで **Move** を使用するときは、引数 rows に正の整数を指定する必要があり、ブックマークは指定できません。つまり、移動できる方向は前方のみです。
> - **Recordset** の最初のレコード、最後のレコード、次のレコード、または前のレコードをカレント レコードにするには、 **MoveFirst**、 **MoveLast**、 **MoveNext**、または **MovePrevious** の各メソッドを使用します。
> - rows に 0 を指定して **Move** を使用すると、カレント レコードの基になるデータを簡単に取得できます。この方法は、カレント レコードにベース テーブルの最新のデータが格納されていることを確認するときに便利です。またこの方法を使用すると、 **[Edit](recordset2-edit-method-dao.md)** または **[AddNew](recordset-addnew-method-dao.md)** に対する保留中の呼び出しが取り消されます。


## <a name="example"></a>例

この例では、 **Move** メソッドを使用して、ユーザーの入力に基づいてレコード ポインターを配置します。

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset2 
       Dim varBookmark As Variant 
       Dim strCommand As String 
       Dim lngMove As Long 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstSuppliers = _ 
          dbsNorthwind.OpenRecordset("SELECT CompanyName, " & _ 
          "City, Country FROM Suppliers ORDER BY CompanyName", _ 
          dbOpenDynaset) 
     
       With rstSuppliers 
          ' Populate recordset. 
          .MoveLast 
          .MoveFirst 
     
          Do While True 
             ' Display information about current record and ask  
             ' how many records to move. 
             strCommand = InputBox( _ 
                "Record " & (.AbsolutePosition + 1) & " of " & _ 
                .RecordCount & vbCr & "Company: " & _ 
                !CompanyName & vbCr & "Location: " & !City & _ 
                ", " & !Country & vbCr & vbCr & _ 
                "Enter number of records to Move " & _ 
                "(positive or negative).") 
     
             If strCommand = "" Then Exit Do 
     
             ' Store bookmark in case the Move doesn't work. 
             varBookmark = .Bookmark 
     
             ' Move method requires parameter of data type Long. 
             lngMove = CLng(strCommand) 
             .Move lngMove 
     
             ' Trap for BOF or EOF. 
             If .BOF Then 
                MsgBox "Too far backward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
             If .EOF Then 
                MsgBox "Too far forward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
          Loop 
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
