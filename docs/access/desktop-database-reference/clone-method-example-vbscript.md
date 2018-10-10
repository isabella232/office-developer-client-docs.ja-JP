---
title: Clone メソッドの使用例 (VBScript)
TOCTitle: Clone Method Example (VBScript)
ms:assetid: b9d49eb9-8da8-dfd2-1c59-35ac70969850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249893(v=office.15)
ms:contentKeyID: 48547357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ce2d2445b6d958f993c419ac9296192bb9dcc0aa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479069"
---
# <a name="clone-method-example-vbscript"></a><span data-ttu-id="c3bbb-102">Clone メソッドの使用例 (VBScript)</span><span class="sxs-lookup"><span data-stu-id="c3bbb-102">Clone Method Example (VBScript)</span></span>


<span data-ttu-id="c3bbb-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3bbb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c3bbb-104">この例では、[Clone](clone-method-ado.md) メソッドを使用して [Recordset](recordset-object-ado.md) のコピーを作成し、ユーザーが各コピーのレコード ポインターを個別に配置できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c3bbb-104">This example uses the [Clone](clone-method-ado.md) method to create copies of a [Recordset](recordset-object-ado.md) and then lets the user position the record pointer of each copy independently.</span></span>

<span data-ttu-id="c3bbb-105">次の例は、Active Server Pages (ASP) で使用してください。</span><span class="sxs-lookup"><span data-stu-id="c3bbb-105">Use the following example in an Active Server Page (ASP).</span></span> <span data-ttu-id="c3bbb-106">この例では、Microsoft Access を含む、Northwind データベースを使用します。</span><span class="sxs-lookup"><span data-stu-id="c3bbb-106">This example uses the Northwind database distributed with Microsoft Access.</span></span> <span data-ttu-id="c3bbb-107">切り取りメモ帳またはほかのテキスト エディターに次のコードを貼り付けして**CloneVBS.asp**として保存します。</span><span class="sxs-lookup"><span data-stu-id="c3bbb-107">Cut and paste the following code to Notepad or another text editor and save it as **CloneVBS.asp**.</span></span> <span data-ttu-id="c3bbb-108">任意のクライアント ブラウザーに結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="c3bbb-108">You can view the result in any client browser.</span></span>

<span data-ttu-id="c3bbb-109">RsCustomerList.Source の行を変更する例を実行するには、「お客様」を RsCustomerList.Source = = 大きなテーブルをカウントするには、「製品」です。</span><span class="sxs-lookup"><span data-stu-id="c3bbb-109">To exercise the example, change the line RsCustomerList.Source = "Customers" to to RsCustomerList.Source = "Products" to count a larger table.</span></span>

```vb 
 
<!-- BeginCloneVBS --> 
<% Language = VBScript %> 
<%' use this meta tag instead of adovbs.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
<HTML> 
<HEAD> 
<TITLE>ADO Clone Method</TITLE> 
</HEAD> 
 
<BODY> 
 
<H1 align="center">ADO Clone Method</H1> 
<HR> 
<% ' to integrate/test this code replace the  
   ' Data Source value in the Connection string%> 
<%  
    ' connection and recordset variables 
    Dim Cnxn, strCnxn 
    Dim rsCustomers, strSQLCustomers 
    Dim rsFirst, rsLast, rsCount 
    Dim rsClone 
    Dim CloneFirst, CloneLast, CloneCount 
 
    ' open connection 
    Set Cnxn = Server.CreateObject("ADODB.Connection") 
    strCnxn = "Provider='sqloledb';Data Source=" & _ 
            Request.ServerVariables("SERVER_NAME") & ";" & _ 
            "Integrated Security='SSPI';Initial Catalog='Northwind';" 
    Cnxn.Open strCnxn 
         
    ' create and open Recordset using object refs 
    Set rsCustomers = Server.CreateObject("ADODB.Recordset") 
    strSQLCustomers = "Customers" 
     
    rsCustomers.ActiveConnection = Cnxn 
    rsCustomers.CursorLocation = adUseClient 
    rsCustomers.CursorType = adOpenKeyset 
    rsCustomers.LockType = adLockOptimistic 
    rsCustomers.Source = strSQLCustomers 
    rsCustomers.Open 
 
    rsCustomers.MoveFirst 
    rsCount = rsCustomers.RecordCount 
    rsFirst = rsCustomers("CompanyName") 
    rsCustomers.MoveLast 
    rsLast = rsCustomers("CompanyName") 
 
    ' create clone 
    Set rsClone = rsCustomers.Clone 
    rsClone.MoveFirst 
    CloneCount = rsClone.RecordCount 
    CloneFirst = rsClone("CompanyName") 
    rsClone.MoveLast 
    CloneLast = rsClone("CompanyName") 
%> 
 
<!-- Display Results --> 
<H3>There Are <%=rsCount%> Records in the original recordset</H3> 
<H3>The first record is <%=rsFirst%> and the last record is <%=rsLast%></H3> 
<BR><HR> 
<H3>There Are <%=CloneCount%> Records in the original recordset</H3> 
<H3>The first record is <%=CloneFirst%> and the last record is <%=CloneLast%></H3> 
<BR><HR> 
<H4>Location of OLEDB Database</H4> 
 
<% 
    ' Show location of DSN data source 
    Response.Write(Cnxn) 
 
    ' Clean up 
    If rsCustomers.State = adStateOpen then 
       rsCustomers.Close 
    End If 
    If rsClone.State = adStateOpen then 
       rsClone.Close 
    End If 
    If Cnxn.State = adStateOpen then 
       Cnxn.Close 
    End If 
    Set rsCustomers = Nothing 
    Set rsClone = Nothing 
    Set Cnxn = Nothing 
%> 
</BODY> 
</HTML> 
<!-- EndCloneVBS --> 
 
```

