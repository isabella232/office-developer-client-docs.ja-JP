---
title: Recordset2.GetRows メソッド (DAO)
TOCTitle: GetRows Method
ms:assetid: e5c0a082-e9d2-359f-fed5-835ab91d2311
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835959(v=office.15)
ms:contentKeyID: 48548367
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 34f6aa2ddd052a9a9ea885c76b5f62b825e8a9e5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476267"
---
# <a name="recordset2getrows-method-dao"></a>Recordset2.GetRows メソッド (DAO)


**適用されます**Access 2013 |。Office 2013

**[Recordset](recordset-object-dao.md)** オブジェクトから複数の行を取得します。

## <a name="syntax"></a>構文

*式*です。GetRows (***NumRows***)

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
<td><p>NumRows</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>取得する行数。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>戻り値

バリアント型 (Variant)

## <a name="remarks"></a>注釈

**GetRows** メソッドは、**Recordset** からレコードをコピーするために使用します。**GetRows** は 2 次元配列を返します。最初の添え字ではフィールドを指定し、2 番目の添え字では行番号を指定します。たとえば次の例では、intField はフィールドを表し、intRecord は行番号を表します。

avarRecords (intField、intRecord)

2 行目の最初のフィールドの値を取得するには、次のようなコードを使用します。

フィールド 1 = avarRecords(0,1)

1 行目の 2 番目のフィールドの値を取得するには、次のようなコードを使用します。

field2 = avarRecords(1,0)

avarRecords 変数は、**GetRows** によってデータが返されると、自動的に 2 次元配列となります。

取得できる行数よりも多くの行を要求すると、 **GetRows** は取得できる行数だけを返します。 配列のサイズは返された行数に応じて決まるため、Visual Basic for Applications の **UBound** 関数を使用すると、 **GetRows** によって実際に取得された行数を確認できます。 たとえば、**バリアント**varA という名前に結果を格納する場合は、実際に返された行の数を決定する次のコードを使用します。

numReturned = UBound(varA,2) + 1

返された最初の行は配列の 0 番目の要素となるため、"+ 1" を付ける必要があります。取得できる行数は、使用できるメモリの容量によって制限されます。テーブルのサイズが大きい場合は、**GetRows** を使用してテーブル全体を配列として取得しないでください。

**GetRows** は、メモ型 (Memo) およびロング バイナリ型 (Long Binary) のフィールドを含む、 **Recordset** のすべてのフィールドが配列として返されるので、クエリを使用して取得する行数を制限した方がよい場合があります。

**GetRows** の呼び出し後、まだ読み込まれていない次の行がカレント レコードになります。 **GetRows**は、numrows の**移動**現在のレコードに同じです。

複数の **GetRows** 呼び出しを使用してすべての行を取得しようとする場合は、 **[EOF](recordset2-eof-property-dao.md)** プロパティを使用して、 **Recordset** の末尾に達していないことを確認してください。 **Recordset** の末尾に達した場合や、要求された範囲のある行を取得できない場合、 **GetRows** は要求された数よりも少ない行を返します。たとえば、10 件のレコードを取得しようといる場合、5 番目のレコードを取得できないときは、 **GetRows** は 4 件のレコードを取得し、5 番目のレコードをカレント レコードにします。この場合、実行時エラーは発生しません。ダイナセット タイプの **Recordset** で別のユーザーがレコードを削除した場合に、このような状況が起こります。このような場合の処理方法については、使用例を参照してください。

## <a name="example"></a>例

この例では、 **GetRows** メソッドを使用して、指定した数の行を **Recordset** から取得し、結果データを配列に設定します。 **GetRows** メソッドでは、 **EOF** に達した場合、および他のユーザーによって削除されたレコードを **GetRows** が取得しようとした場合に、指定よりも少ない数の行が返されます。2 番目の場合のみ、 **False** が返されます。このプロシージャを実行するには、GetRowsOK 関数が必要です。

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
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
     
    Function GetRowsOK(rstTemp As Recordset2, _ 
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
