---
title: ストリームと永続性
TOCTitle: Streams and Persistence
ms:assetid: 564fc098-52bf-77d7-9d48-75186483e3fe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249289(v=office.15)
ms:contentKeyID: 48544949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a90031ac2f6d573631063edb0faf4893c2320d03
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944383"
---
# <a name="streams-and-persistence"></a>ストリームと永続性


**適用されます**Access 2013、Office 2013。

[レコード セット](recordset-object-ado.md)オブジェクト[の保存](save-method-ado.md)方法、店舗、*引き続き発生する*ファイル、および[Open](open-method-ado-recordset.md)メソッドには、**レコード セット**は、そのファイルから**レコード セット**を復元します。

ADO 2.5 では、 **Save** メソッドと **Open** メソッドを使用して、 **Recordset** を [Stream](stream-object-ado.md) オブジェクトに永続化することもできます。この機能は、リモート データ サービス (RDS) および Active Server Pages (ASP) と併せて使用すると特に役に立ちます。

ASP ページでの永続性の使用方法の詳細については、最新の ASP のマニュアルを参照してください。

以下では、 **Stream** オブジェクトと永続性を使用する方法についてのシナリオをいくつか示します。

## <a name="scenario-1"></a>シナリオ 1

このシナリオでは、 **Recordset** をファイルに保存した後、 **Stream** に単純に保存します。その後、永続化したストリームを別の **Recordset** で開きます。

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

## <a name="scenario-2"></a>シナリオ 2

このシナリオでは、 **Recordset** を **Stream** に XML 形式で永続化します。その後、検査、操作、または表示できる文字列として **Stream** を読み取ります。

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

## <a name="scenario-3"></a>シナリオ 3

この例では、 **Recordset** を XML として **Response** オブジェクトに直接永続化する ASP コードを示します。

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

## <a name="scenario-4"></a>シナリオ 4

このシナリオの ASP コードは、ADTG 形式の **Recordset** の内容をクライアントに書き出します。 [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) は、このデータを使用して、接続されていない **Recordset** を作成できます。

RDS [DataControl](datacontrol-object-rds.md) の新しいプロパティである [URL](url-property-rds.md) は、 **Recordset** を生成する .asp ページを示します。つまり、RDS でサーバー側 **DataFactory** オブジェクトを使用しなくても、またはユーザーがビジネス オブジェクトを作成しなくても、 [Recordset](datafactory-object-rdsserver.md) オブジェクトを取得できます。これにより、RDS のプログラミング モデルはたいへん簡単になります。

以下は、https://server/directory/recordset.asp: という名前のサーバー側コードです。

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

以下は、クライアント側コードです。

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

必要に応じて、クライアントで **Recordset** オブジェクトを使用することもできます。

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

