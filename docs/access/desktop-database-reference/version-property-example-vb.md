---
<span data-ttu-id="3c1dc-101"><<<<<<< ヘッド タイトル: バージョン プロパティの使用例 (VB) TOCTitle: バージョン プロパティの使用例 (VB) === タイトル: バージョン プロパティの使用例 (VB) TOCTitle: バージョン プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="3c1dc-101"><<<<<<< HEAD title: Version Property Example (VB) TOCTitle: Version Property Example (VB) ======= title: Version property example (VB) TOCTitle: Version property example (VB)</span></span>
>>>>>>> <span data-ttu-id="3c1dc-102">マスターの ms:assetid: ffb7b04a-55b9-fa2f-41ec-44af225bd15f ms:mtpsurl: https://msdn.microsoft.com/library/JJ250315(v=office.15) ms:contentKeyID: 48548968 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="3c1dc-102">master ms:assetid: ffb7b04a-55b9-fa2f-41ec-44af225bd15f ms:mtpsurl: https://msdn.microsoft.com/library/JJ250315(v=office.15) ms:contentKeyID: 48548968 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="3c1dc-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="3c1dc-103"><<<<<<< HEAD</span></span>
# <a name="version-property-example-vb"></a><span data-ttu-id="3c1dc-104">Version プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="3c1dc-104">Version Property Example (VB)</span></span>
=======
# <a name="version-property-example-vb"></a><span data-ttu-id="3c1dc-105">バージョン プロパティの使用例 (VB)</span><span class="sxs-lookup"><span data-stu-id="3c1dc-105">Version property example (VB)</span></span>
>>>>>>> <span data-ttu-id="3c1dc-106">master</span><span class="sxs-lookup"><span data-stu-id="3c1dc-106">master</span></span>


<span data-ttu-id="3c1dc-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c1dc-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3c1dc-p101">この例では、[Connection](version-property-ado.md) オブジェクトの [Version](connection-object-ado.md) プロパティを使用して、現在の ADO のバージョンを表示します。また、動的プロパティを使用して、次の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="3c1dc-p101">This example uses the [Version](version-property-ado.md) property of a [Connection](connection-object-ado.md) object to display the current ADO version. It also uses several dynamic properties to show:</span></span>

  - <span data-ttu-id="3c1dc-110">現在の DBMS の名前およびバージョン</span><span class="sxs-lookup"><span data-stu-id="3c1dc-110">the current DBMS name and version.</span></span>

  - <span data-ttu-id="3c1dc-111">OLE DB のバージョン</span><span class="sxs-lookup"><span data-stu-id="3c1dc-111">OLE DB version.</span></span>

  - <span data-ttu-id="3c1dc-112">プロバイダーの名前およびバージョン</span><span class="sxs-lookup"><span data-stu-id="3c1dc-112">provider name and version.</span></span>

  - <span data-ttu-id="3c1dc-113">ODBC のバージョン</span><span class="sxs-lookup"><span data-stu-id="3c1dc-113">ODBC version.</span></span>

  - <span data-ttu-id="3c1dc-114">ODBC ドライバーの名前およびバージョン</span><span class="sxs-lookup"><span data-stu-id="3c1dc-114">ODBC driver name and version.</span></span>

<!-- end list -->

```vb 
 
'BeginVersionVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strVersionInfo As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 strVersionInfo = "ADO Version: " & Cnxn.Version & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Name: " & Cnxn.Properties("DBMS Name") & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Version: " & Cnxn.Properties("DBMS Version") & vbCr 
 strVersionInfo = strVersionInfo & "OLE DB Version: " & Cnxn.Properties("OLE DB Version") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Name: " & Cnxn.Properties("Provider Name") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Version: " & Cnxn.Properties("Provider Version") & vbCr 
 
 MsgBox strVersionInfo 
 
 ' clean up 
 Cnxn.Close 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndVersionVB 
```

