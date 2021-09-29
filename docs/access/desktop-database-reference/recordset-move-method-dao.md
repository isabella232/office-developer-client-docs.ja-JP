---
title: Recordset.Move メソッド (DAO)
TOCTitle: Move Method
ms:assetid: 21ca5ab5-ff71-1ae8-21b3-8991d5f795cf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191697(v=office.15)
ms:contentKeyID: 48543689
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052941
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 462a6f898770db280356d341590469d5e56cb727
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606248"
---
# <a name="recordsetmove-method-dao"></a>Recordset.Move メソッド (DAO)

**適用先**: Access 2013、Office 2013

現在のレコードの位置を **[[Recordset]](recordset-object-dao.md)** オブジェクトに移動します。

## <a name="syntax"></a>構文

*式* .Move(**Rows**, _StartBookmark_)

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
<td><p><em>Rows</em></p></td>
<td><p>必須</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>位置を移動する行数。rows が 0 より大きい場合は、前方 (ファイルの末尾) に向かって位置が移動します。rows が 0 より小さい場合は、後方 (ファイルの先頭) に向かって位置が移動します。</p></td>
</tr>
<tr class="even">
<td><p><em>StartBookmark</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>ブックマークを示す値。startbookmark を指定した場合、このブックマークが移動の開始位置となります。それ以外の場合は、カレント レコードが移動の開始位置となります。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**Move** を使用して、カレント レコードを参照するポインターを最初のレコードよりも前に設定すると、カレント レコードを参照するポインターはファイルの先頭に移動します。 **Recordset** にレコードが含まれておらず、 **[BOF](recordset-bof-property-dao.md)** プロパティが **True** の場合は、このメソッドを使用して後方に移動しようとするとエラーが発生します。

**Move** を使用して、カレント レコードを参照するポインターを最後のレコードよりも後ろに設定すると、カレント レコードを参照するポインターはファイルの末尾に移動します。 **Recordset** にレコードが含まれておらず、 **[EOF](recordset-eof-property-dao.md)** プロパティが **True** の場合は、このメソッドを使用して前方に移動しようとするとエラーが発生します。

**BOF** プロパティまたは **EOF** プロパティが **True** の場合に、有効なブックマークを指定せずに **Move** メソッドを使用しようとすると、実行時エラーが発生します。

> [!NOTE]
> - 前方スクロール タイプの **Recordset** オブジェクトで **Move** を使用するときは、引数 rows に正の整数を指定する必要があり、ブックマークは指定できません。つまり、移動できる方向は前方のみです。
> - **Recordset** の最初のレコード、最後のレコード、次のレコード、または前のレコードをカレント レコードにするには、 **MoveFirst**、 **MoveLast**、 **MoveNext**、または **MovePrevious** の各メソッドを使用します。
> - rows に 0 を指定して **Move** を使用すると、カレント レコードの基になるデータを簡単に取得できます。この方法は、カレント レコードにベース テーブルの最新のデータが格納されていることを確認するときに便利です。またこの方法を使用すると、 **[Edit](recordset2-edit-method-dao.md)** または **[AddNew](recordset-addnew-method-dao.md)** に対する保留中の呼び出しが取り消されます。


## <a name="example"></a>例

この例では、**Move** メソッドを使用して、ユーザーの入力に基づいてレコード ポインターを配置します。

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset 
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
