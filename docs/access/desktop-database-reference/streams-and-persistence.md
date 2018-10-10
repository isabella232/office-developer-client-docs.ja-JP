---
title: ストリームと永続性
TOCTitle: Streams and Persistence
ms:assetid: 564fc098-52bf-77d7-9d48-75186483e3fe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249289(v=office.15)
ms:contentKeyID: 48544949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d47d7bb4d8e9243d48daf4ad7947cef2416d4004
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478652"
---
# <a name="streams-and-persistence"></a><span data-ttu-id="b3171-102">ストリームと永続性</span><span class="sxs-lookup"><span data-stu-id="b3171-102">Streams and Persistence</span></span>


<span data-ttu-id="b3171-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3171-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b3171-104">[レコード セット](recordset-object-ado.md)オブジェクト[の保存](save-method-ado.md)方法、店舗、*引き続き発生する*ファイル、および[Open](open-method-ado-recordset.md)メソッドには、**レコード セット**は、そのファイルから**レコード セット**を復元します。</span><span class="sxs-lookup"><span data-stu-id="b3171-104">The [Recordset](recordset-object-ado.md) object [Save](save-method-ado.md) method stores, or *persists*, a **Recordset** in a file, and the [Open](open-method-ado-recordset.md) method restores the **Recordset** from that file.</span></span>

<span data-ttu-id="b3171-p101">ADO 2.5 では、 **Save** メソッドと **Open** メソッドを使用して、 **Recordset** を [Stream](stream-object-ado.md) オブジェクトに永続化することもできます。この機能は、リモート データ サービス (RDS) および Active Server Pages (ASP) と併せて使用すると特に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="b3171-p101">With ADO 2.5, the **Save** and **Open** methods can persist a **Recordset** to a [Stream](stream-object-ado.md) object as well. This feature is especially useful when working with Remote Data Service (RDS) and Active Server Pages (ASP).</span></span>

<span data-ttu-id="b3171-107">ASP ページでの永続性の使用方法の詳細については、最新の ASP のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3171-107">For more information about how persistence can be used by itself on ASP pages, see the current ASP documentation.</span></span>

<span data-ttu-id="b3171-108">以下では、 **Stream** オブジェクトと永続性を使用する方法についてのシナリオをいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="b3171-108">The following are a few scenarios that show how **Stream** objects and persistence can be used.</span></span>

## <a name="scenario-1"></a><span data-ttu-id="b3171-109">シナリオ 1</span><span class="sxs-lookup"><span data-stu-id="b3171-109">Scenario 1</span></span>

<span data-ttu-id="b3171-p102">このシナリオでは、 **Recordset** をファイルに保存した後、 **Stream** に単純に保存します。その後、永続化したストリームを別の **Recordset** で開きます。</span><span class="sxs-lookup"><span data-stu-id="b3171-p102">This scenario simply saves a **Recordset** to a file and then to a **Stream**. It then opens the persisted stream into another **Recordset**.</span></span>

```vb 
 
Dim rs1 As ADODB.Recordset 
Dim rs2 As ADODB.Recordset 
Dim stm As ADODB.Stream 
 
Set rs1 = New ADODB.Recordset 
Set rs2 = New ADODB.Recordset 
Set stm = New ADODB.Stream 
 
rs1.Open "SELECT * FROM Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""", adopenStatic, adLockReadOnly, adCmdText 
rs1.Save "c:\myfolder\mysubfolder\myrs.xml", adPersistXML 
rs1.Save stm, adPersistXML 
rs2.Open stm 
```

## <a name="scenario-2"></a><span data-ttu-id="b3171-112">シナリオ 2</span><span class="sxs-lookup"><span data-stu-id="b3171-112">Scenario 2</span></span>

<span data-ttu-id="b3171-p103">このシナリオでは、 **Recordset** を **Stream** に XML 形式で永続化します。その後、検査、操作、または表示できる文字列として **Stream** を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="b3171-p103">This scenario persists a **Recordset** into a **Stream** in XML format. It then reads the **Stream** into a string that you can examine, manipulate, or display.</span></span>

```vb 
 
Dim rs As ADODB.Recordset 
Dim stm As ADODB.Stream 
Dim strRst As String 
 
Set rs = New ADODB.Recordset 
Set stm = New ADODB.Stream 
 
' Open, save, and close the recordset. 
rs.Open "SELECT * FROM Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""" 
rs.Save stm, adPersistXML 
rs.Close 
Set rs = nothing 
 
' Put saved Recordset into a string variable. 
strRst = stm.ReadText(adReadAll) 
 
' Examine, manipulate, or display the XML data. 
... 
```

## <a name="scenario-3"></a><span data-ttu-id="b3171-115">シナリオ 3</span><span class="sxs-lookup"><span data-stu-id="b3171-115">Scenario 3</span></span>

<span data-ttu-id="b3171-116">この例では、 **Recordset** を XML として **Response** オブジェクトに直接永続化する ASP コードを示します。</span><span class="sxs-lookup"><span data-stu-id="b3171-116">This example code shows ASP code persisting a **Recordset** as XML directly to the **Response** object:</span></span>

```vb 
 
... 
<% 
response.ContentType = "text/xml" 
 
' Create and open a Recordset. 
Set rs = Server.CreateObject("ADODB.Recordset") 
rs.Open "select * from Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""" 
 
' Save Recordset directly into output stream. 
rs.Save Response, adPersistXML 
 
' Close Recordset. 
rs.Close 
Set rs = nothing 
%> 
... 
```

## <a name="scenario-4"></a><span data-ttu-id="b3171-117">シナリオ 4</span><span class="sxs-lookup"><span data-stu-id="b3171-117">Scenario 4</span></span>

<span data-ttu-id="b3171-p104">このシナリオの ASP コードは、ADTG 形式の **Recordset** の内容をクライアントに書き出します。 [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) は、このデータを使用して、接続されていない **Recordset** を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b3171-p104">In this scenario, ASP code writes the contents of the **Recordset** in ADTG format to the client. The [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) can use this data to create a disconnected **Recordset**.</span></span>

<span data-ttu-id="b3171-p105">RDS [DataControl](datacontrol-object-rds.md) の新しいプロパティである [URL](url-property-rds.md) は、 **Recordset** を生成する .asp ページを示します。つまり、RDS でサーバー側 **DataFactory** オブジェクトを使用しなくても、またはユーザーがビジネス オブジェクトを作成しなくても、 [Recordset](datafactory-object-rdsserver.md) オブジェクトを取得できます。これにより、RDS のプログラミング モデルはたいへん簡単になります。</span><span class="sxs-lookup"><span data-stu-id="b3171-p105">A new property on the RDS [DataControl](datacontrol-object-rds.md), [URL](url-property-rds.md), points to the .asp page that generates the **Recordset**. This means a **Recordset** object can be obtained without RDS using the server-side [DataFactory](datafactory-object-rdsserver.md) object or the user writing a business object. This simplifies the RDS programming model significantly.</span></span>

<span data-ttu-id="b3171-123">以下は、https://server/directory/recordset.asp: という名前のサーバー側コードです。</span><span class="sxs-lookup"><span data-stu-id="b3171-123">Server-side code, named https://server/directory/recordset.asp:</span></span>

```vb 
 
<% 
Dim rs 
Set rs = Server.CreateObject("ADODB.Recordset") 
rs.Open "select au_fname, au_lname, phone from Authors", ""& _ 
 "Provider=sqloledb;Data Source=MyServer;" & _ 
 "Initial Catalog=Pubs;Integrated Security=SSPI;" 
response.ContentType = "multipart/mixed" 
rs.Save response, adPersistADTG 
%> 
```

<span data-ttu-id="b3171-124">以下は、クライアント側コードです。</span><span class="sxs-lookup"><span data-stu-id="b3171-124">Client-side code:</span></span>

```html 
 
<HTML> 
<HEAD> 
<TITLE>RDS Query Page</TITLE> 
</HEAD> 
<body> 
<CENTER> 
<H1>Remote Data Service 2.5</H1> 
<TABLE DATASRC="#DC1"> 
 <TR> 
 <TD><SPAN DATAFLD="au_fname"></SPAN></TD> 
 <TD><SPAN DATAFLD="au_lname"></SPAN></TD> 
 <TD><SPAN DATAFLD="phone"></SPAN></TD> 
 </TR> 
</TABLE> 

<BR> 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
 ID=DC1 HEIGHT=1 WIDTH = 1> 
 <PARAM NAME="URL" VALUE="https://server/directory/recordset.asp"> 
</OBJECT> 
 
</SCRIPT> 
</BODY> 
</HTML> 
```

<span data-ttu-id="b3171-125">必要に応じて、クライアントで **Recordset** オブジェクトを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="b3171-125">Developers also have the option of using a **Recordset** object on the client:</span></span>

```vb
... 
function GetRs() 
 { 
 rs = CreateObject("ADODB.Recordset"); 
 rs.Open "https://server/directory/recordset.asp" 
 DC1.SourceRecordset = rs; 
 } 
... 
```

