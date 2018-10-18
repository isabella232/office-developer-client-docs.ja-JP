---
<<<<<<< ヘッド タイトル: 並べ替えのプロパティの使用例 (VB) TOCTitle: 並べ替えのプロパティの使用例 (VB) === タイトル: 並べ替えのプロパティの使用例 (VB) TOCTitle: 並べ替えプロパティの使用例 (VB)
>>>>>>> マスターの ms:assetid: 6f981e5e-7ee8-e1e7-bea9-7c2081400391 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249440(v=office.15) ms:contentKeyID: 48545539 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="sort-property-example-vb"></a>Sort プロパティの使用例 (VB)
=======
# <a name="sort-property-example-vb"></a>並べ替えプロパティの使用例 (VB)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

この例では、[レコード セット](recordset-object-ado.md)オブジェクトの[Sort](sort-property-ado.md)プロパティを使用して、 ***Pubs***データベースの***Authors***テーブルから派生した**レコード セット**の行の順序を変更します。 2 次ユーティリティ ルーチンで各行を出力します。

```vb 
 
'BeginSortVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' connection and recordset variables 
 Dim Cnxn As New ADODB.Connection 
 Dim rstAuthors As New ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLAuthors As String 
 
 Dim strTitle As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open client-side recordset to enable sort method 
 Set rstAuthors = New ADODB.Recordset 
 rstAuthors.CursorLocation = adUseClient 
 strSQLAuthors = "SELECT * FROM Authors" 
 rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 ' sort the recordset last name ascending 
 rstAuthors.Sort = "au_lname ASC, au_fname ASC" 
 ' show output 
 Debug.Print "Last Name Ascending:" 
 Debug.Print "First Name Last Name" & vbCr 
 
 rstAuthors.MoveFirst 
 Do Until rstAuthors.EOF 
 Debug.Print rstAuthors!au_fname & " " & rstAuthors!au_lname 
 rstAuthors.MoveNext 
 Loop 
 
 ' sort the recordset last name descending 
 rstAuthors.Sort = "au_lname DESC, au_fname ASC" 
 ' show output 
 Debug.Print "Last Name Descending" 
 Debug.Print "First Name Last Name" & vbCr 
 
 Do Until rstAuthors.EOF 
 Debug.Print rstAuthors!au_fname & " " & rstAuthors!au_lname 
 rstAuthors.MoveNext 
 Loop 
 
 ' clean up 
 rstAuthors.Close 
 Cnxn.Close 
 Set rstAuthors = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstAuthors Is Nothing Then 
 If rstAuthors.State = adStateOpen Then rstAuthors.Close 
 End If 
 Set rstAuthors = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndSortVB 
```

次のコードは、与えられたタイトルと、指定された **Recordset** の内容を出力する 2 次ユーティリティ ルーチンです。

```vb 
 
Attribute VB_Name = "Sort" 
```

