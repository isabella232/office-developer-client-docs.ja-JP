---
title: Recordset.GetRows メソッド (DAO)
TOCTitle: GetRows method
ms:assetid: 59f6e4f0-e7b1-db60-31c7-3338b66d3345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194427(v=office.15)
ms:contentKeyID: 48545031
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053362
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 37714f7581631a1cb095c3d2c8564d9a4f8afa6c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606283"
---
# <a name="recordsetgetrows-method-dao"></a>Recordset.GetRows メソッド (DAO)

**適用先**: Access 2013、Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクトから複数行を取得します。

## <a name="syntax"></a>構文

*式* .GetRows (***NumRows***)

*式* **Recordset** オブジェクトを表す変数です。

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
<td><p><em>NumRows</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>取得する行数。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

バリアント型

## <a name="remarks"></a>注釈

**GetRows** メソッドは、**Recordset** からレコードをコピーするために使用します。**GetRows** は 2 次元配列を返します。最初の添え字ではフィールドを指定し、2 番目の添え字では行番号を指定します。たとえば `intField` はフィールドを表し、`intRecord` では行番号を表します。

`avarRecords(intField, intRecord)`

2 番目の行に含まれる最初のフィールドの値を取得するには、次のようなコードを使用します。

`field1 = avarRecords(0,1)`

最初の行に含まれる 2 番目のフィールドの値を取得するには、次のようなコードを使用します。

`field2 = avarRecords(1,0)`

**GetRows** がデータを返すと、avarRecords 変数は自動的に 2 次元配列になります。

取得できる行数よりも多くの行を要求すると、**GetRows** は取得できる行数だけを返します。配列のサイズは返された行数に応じて決まるため、Visual Basic for Applications の **UBound** 関数を使用すると、**GetRows** によって実際に取得された行数を確認できます。たとえば、取得した結果を varA という **バリアント型 (Variant)** の変数に代入した場合は、次のコードを使用して、実際に取得した行数を確認できます。

`numReturned = UBound(varA,2) + 1`

返された最初の行は配列の 0 番目の要素となるため、"+ 1" を付ける必要があります。取得できる行数は、使用できるメモリの容量によって制限されます。テーブルのサイズが大きい場合は、**GetRows** を使用してテーブル全体を配列として取得しないでください。

**GetRows** では、メモやロング バイナリを含む **Recordset** のすべてのフィールドが配列として返されるため、取得するフィールドを制限するクエリを使用すると有効な場合があります。

**GetRows** の呼び出し後、まだ読み込まれていない次の行がカレント レコードになります。つまり、**GetRows** を使用した場合のカレント レコードへの影響は、**Move** numrows の場合と同じです。

すべての行を取得するために **GetRows** を複数回呼び出す場合は、 **[EOF](recordset-eof-property-dao.md)** プロパティを使用して、 **Recordset** の末尾まで確実に読み込まれるようにします。 **GetRows** は、 **Recordset** の末尾まで到達した場合や、要求された範囲内の行を読み込むことができない場合は、要求された数よりも少ないレコードを返します。たとえば、10 個のレコードを取得しようとしているが、5 番目のレコードを取得できない場合、 **GetRows** は 4 個のレコードを返し、5 番目のレコードをカレント レコードにします。この場合、実行時エラーは発生しません。このような現象は、ダイナセット タイプの **Recordset** で、他のユーザーがレコードを削除した場合などに発生します。このような場合の処理方法については、使用例を参照してください。

## <a name="example"></a>例

次の例では、 **GetRows** メソッドを使用して、指定された数の行を **Recordset** から取得し、結果データを配列に格納します。 **GetRows** メソッドは、 **EOF** に到達したとき、または他のユーザーが削除したレコードを **GetRows** で取得しようとしたときの 2 つの場合に、要求された数よりも少ない行を返します。この関数は、後者の場合にのみ **False** を返します。このプロシージャを実行するには、GetRowsOK 関数が必要です。

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim intRows As Integer 
     Dim avarRecords As Variant 
     Dim intRecord As Integer 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT FirstName, LastName, Title " & _ 
     "FROM Employees ORDER BY LastName", dbOpenSnapshot) 
     
     With rstEmployees 
     Do While True 
     ' Get user input for number of rows. 
     strMessage = "Enter number of rows to retrieve." 
     intRows = Val(InputBox(strMessage)) 
     
     If intRows <= 0 Then Exit Do 
     
     ' If GetRowsOK is successful, print the results, 
     ' noting if the end of the file was reached. 
     If GetRowsOK(rstEmployees, intRows, _ 
     avarRecords) Then 
     If intRows > UBound(avarRecords, 2) + 1 Then 
     Debug.Print "(Not enough records in " & _ 
     "Recordset to retrieve " & intRows & _ 
     " rows.)" 
     End If 
     Debug.Print UBound(avarRecords, 2) + 1 & _ 
     " records found." 
     
     ' Print the retrieved data. 
     For intRecord = 0 To UBound(avarRecords, 2) 
     Debug.Print " " & _ 
     avarRecords(0, intRecord) & " " & _ 
     avarRecords(1, intRecord) & ", " & _ 
     avarRecords(2, intRecord) 
     Next intRecord 
     Else 
     ' Assuming the GetRows error was due to data 
     ' changes by another user, use Requery to 
     ' refresh the Recordset and start over. 
     If .Restartable Then 
     If MsgBox("GetRows failed--retry?", _ 
     vbYesNo) = vbYes Then 
     .Requery 
     Else 
     Debug.Print "GetRows failed!" 
     Exit Do 
     End If 
     Else 
     Debug.Print "GetRows failed! " & _ 
     "Recordset not Restartable!" 
     Exit Do 
     End If 
     End If 
     
     ' Because using GetRows leaves the current record 
     ' pointer at the last record accessed, move the 
     ' pointer back to the beginning of the Recordset 
     ' before looping back for another search. 
     .MoveFirst 
     Loop 
     End With 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function GetRowsOK(rstTemp As Recordset, _ 
     intNumber As Integer, avarData As Variant) As Boolean 
     
     ' Store results of GetRows method in array. 
     avarData = rstTemp.GetRows(intNumber) 
     ' Return False only if fewer than the desired number of 
     ' rows were returned, but not because the end of the 
     ' Recordset was reached. 
     If intNumber > UBound(avarData, 2) + 1 And _ 
     Not rstTemp.EOF Then 
     GetRowsOK = False 
     Else 
     GetRowsOK = True 
     End If 
     
    End Function
```
