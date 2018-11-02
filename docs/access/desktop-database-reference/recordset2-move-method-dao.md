---
title: Recordset2.Move メソッド (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8ed9eb021df9d4c82473f1924a539787680f76a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928804"
---
# <a name="recordset2move-method-dao"></a>Recordset2.Move メソッド (DAO)


**適用されます**Access 2013、Office 2013。

**[Recordset](recordset-object-dao.md)** オブジェクトでカレント レコードの位置を移動します。

## <a name="syntax"></a>構文

*式*です。移動 (***行***、 ***StartBookmark***)

*式***Recordset2**オブジェクトを表す変数です。

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
<td><p>行</p></td>
<td><p>必須</p></td>
<td><p><strong>長整数型 (Long)</strong></p></td>
<td><p>位置を移動する行数。rows が 0 より大きい場合は、前方 (ファイルの末尾) に向かって位置が移動します。rows が 0 より小さい場合は、後方 (ファイルの先頭) に向かって位置が移動します。</p></td>
</tr>
<tr class="even">
<td><p>StartBookmark</p></td>
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
> <UL>
> <LI>
> <P>前方スクロール タイプの <STRONG>Recordset</STRONG> オブジェクトで <STRONG>Move</STRONG> を使用するときは、引数 rows に正の整数を指定する必要があり、ブックマークは指定できません。つまり、移動できる方向は前方のみです。</P>
> <LI>
> <P><STRONG>Recordset</STRONG> の最初のレコード、最後のレコード、次のレコード、または前のレコードをカレント レコードにするには、 <STRONG>MoveFirst</STRONG>、 <STRONG>MoveLast</STRONG>、 <STRONG>MoveNext</STRONG>、または <STRONG>MovePrevious</STRONG> の各メソッドを使用します。</P>
> <LI>
> <P>rows に 0 を指定して <STRONG>Move</STRONG> を使用すると、カレント レコードの基になるデータを簡単に取得できます。この方法は、カレント レコードにベース テーブルの最新のデータが格納されていることを確認するときに便利です。またこの方法を使用すると、 <STRONG><A href="recordset2-edit-method-dao.md">Edit</A></STRONG> または <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> に対する保留中の呼び出しが取り消されます。</P></LI></UL>



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
