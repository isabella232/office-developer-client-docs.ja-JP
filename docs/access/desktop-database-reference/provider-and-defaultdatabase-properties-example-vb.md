---
<<<<<<< ヘッド タイトル: プロバイダーと DefaultDatabase プロパティの使用例 (VB) TOCTitle: プロバイダーと DefaultDatabase プロパティの使用例 (VB) === タイトル: プロバイダーと DefaultDatabase プロパティの使用例 (VB) TOCTitle: プロバイダーとDefaultDatabase プロパティの使用例 (VB)
>>>>>>> マスターの ms:assetid: 337b90e6-851d-2101-0671-50c4173aec13 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249104(v=office.15) ms:contentKeyID: 48544107 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="provider-and-defaultdatabase-properties-example-vb"></a>Provider プロパティと DefaultDatabase プロパティの使用例 (VB)
=======
# <a name="provider-and-defaultdatabase-properties-example-vb"></a>プロバイダーと DefaultDatabase プロパティの使用例 (VB)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

この例では、異なるプロバイダーを使用する 3 つの [Connection](provider-property-ado.md) オブジェクトを開くことによって、 [Provider](connection-object-ado.md) プロパティの機能を示します。また、 [DefaultDatabase](defaultdatabase-property-ado.md) プロパティを使用して、Microsoft ODBC Provider の既定のデータベースを設定します。

```vb 
 
'BeginProviderVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection strings 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn1 As ADODB.Connection 
 Dim Cnxn2 As ADODB.Connection 
 Dim Cnxn3 As ADODB.Connection 
 Dim strCnxn As String 
 
 ' Open a connection using the Microsoft ODBC provider 
 Set Cnxn1 = New ADODB.Connection 
 Cnxn1.ConnectionString = "driver={SQL Server};server='MySqlServer';" & _ 
 "user id='MyUserID';password='MyPassword';" 
 Cnxn1.Open strCnxn 
 Cnxn1.DefaultDatabase = "Pubs" 
 
 ' Display the provider 
 MsgBox "Cnxn1 provider: " & Cnxn1.Provider 
 
 ' Open a connection using the Microsoft Jet provider 
 Set Cnxn2 = New ADODB.Connection 
 Cnxn2.Provider = "Microsoft.Jet.OLEDB.4.0" 
 Cnxn2.Open "C:\Program Files\Microsoft Office\Office\Samples\northwind.mdb", _ 
 "MyUserID", "MyPassword" 
 
 ' Display the provider. 
 MsgBox "Cnxn2 provider: " & Cnxn2.Provider 
 
 ' Open a connection using the Microsoft SQL Server provider 
 Set Cnxn3 = New ADODB.Connection 
 Cnxn3.Provider = "sqloledb" 
 Cnxn3.Open "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 
 ' Display the provider 
 MsgBox "Cnxn3 provider: " & Cnxn3.Provider 
 
 ' clean up 
 Cnxn1.Close 
 Cnxn2.Close 
 Cnxn3.Close 
 Set Cnxn1 = Nothing 
 Set Cnxn2 = Nothing 
 Set Cnxn3 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 If Not Cnxn1 Is Nothing Then 
 If Cnxn1.State = adStateOpen Then Cnxn1.Close 
 End If 
 Set Cnxn1 = Nothing 
 
 If Not Cnxn2 Is Nothing Then 
 If Cnxn2.State = adStateOpen Then Cnxn2.Close 
 End If 
 Set Cnxn2 = Nothing 
 
 If Not Cnxn3 Is Nothing Then 
 If Cnxn3.State = adStateOpen Then Cnxn3.Close 
 End If 
 Set Cnxn3 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndProviderVB 
```

