---
title: Workspace.OpenConnection メソッド (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 9d97f298-a2d5-3b91-2efd-57f06fbd4654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198249(v=office.15)
ms:contentKeyID: 48546628
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 58416329d288263ee1cd07acb21fc90500c9685f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611316"
---
# <a name="workspaceopenconnection-method-dao"></a>Workspace.OpenConnection メソッド (DAO)

**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*.OpenConnection(***Name** _, _*_Options_*_, _*_ReadOnly_*_,__*_ Connect **)

*expression*: **Workspace** オブジェクトを表す変数。

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
<td><p><em>名前</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>文字列式を指定します。「解説」の説明を参照してください。</p></td>
</tr>
<tr class="even">
<td><p><em>オプション</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>「解説」に記載されている接続のさまざまなオプションを設定します。ODBC ドライバー マネージャーは、この値に基づき、データ ソース名 (DSN)、ユーザー名、パスワードなどの接続情報の指定をユーザーに求めます。</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> に設定すると、接続が読み取り専用アクセスで開かれ、 <strong>False</strong> (既定値) に設定すると、読み取り/書き込みアクセスで開かれます。</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>ODBC 接続文字列です。 この文字列の固有の要素および構文については、 <strong><a href="connection-connect-property-dao.md">Connect</a></strong> プロパティのトピックを参照してください。 前に追加された &quot; ODBC が &quot; 必要です。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

Connection

## <a name="remarks"></a>注釈

**OpenConnection** メソッドは、ODBCDirect ワークスペースから ODBC データ ソースへの接続を確立するために使用します。**OpenConnection** メソッドは、**OpenDatabase** と似ていますが、同じではありません。主な違いは、**OpenConnection** が ODBCDirect ワークスペースでしか使用できないことです。

connect 引数に登録済みの ODBC データ ソース名 (DSN) を指定した場合、name 引数には任意の有効な文字列を指定できます。**また、Connection** オブジェクトの **Name** プロパティも指定します。 有効な DSN が connect 引数に含まれていない場合、name は有効な ODBC DSN を参照する必要があります。これは Name プロパティにも **指定** されます。 名前も接続も有効な DSN が含まれている場合は、ODBC ドライバー マネージャーを (options 引数を使用して) 設定して、必要な接続情報をユーザーに要求できます。 この場合、ユーザーが指定した DSN が **Name** プロパティの値となります。

options 引数は、ユーザーに接続の確立を求めるメッセージを表示するかどうか、および接続を非同期的に開くかどうかを決定します。 次のいずれかの定数を使用できます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDriverNoPrompt</strong></p></td>
<td><p>ODBC ドライバー マネージャーは、<em>name</em> および <em>connect</em> に指定された接続文字列を使用します。情報が不足していると、実行時エラーが発生します。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverPrompt</strong></p></td>
<td><p>ODBC ドライバー マネージャーは、<em>dhname</em> または <em>connect</em> で指定された関連情報を示す [<strong>接続する ODBC データ ソース</strong>] ダイアログ ボックスを開きます。接続文字列は、ユーザーがダイアログ ボックスで選択した DSN を使用して作成されますが、ユーザーが DSN を指定しなかった場合は、既定の DSN が使用されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDriverComplete</strong></p></td>
<td><p>既定値です。引数 <em>connect</em> で接続の確立に必要な情報がすべて指定されている場合、ODBC ドライバー マネージャーは <em>connect</em> で指定されている文字列を使用します。指定されていない情報がある場合は、<strong>dbDriverPrompt</strong> を指定したときと同じ動作を行います。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverCompleteRequired</strong></p></td>
<td><p>このオプションを指定した場合の動作は <strong>dbDriverComplete</strong> の場合と似ていますが、接続を確立するために不足している情報についてのみユーザー入力を求める点が異なります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>メソッドを非同期で実行します。この定数は、<em>options</em> で他の任意の定数と共に使用できます。</p></td>
</tr>
</tbody>
</table>

<br/>

**OpenConnection** は、接続に関する情報を含む **Connection** オブジェクトを返します。 **Connection** オブジェクトは **[Database](database-object-dao.md)** オブジェクトに似ています。主な違いは、 **Database** オブジェクトは、通常、データベースを表すものの、Microsoft Access ワークスペースから ODBC データ ソースへの接続を表すためにも使用できることです。

## <a name="example"></a>例

この例では、**OpenConnection** メソッドで 3 つのパラメーターを使用して、それぞれの **Connection** オブジェクトを開きます。

```vb 
Sub OpenConnectionX() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim conPubs2 As Connection 
 Dim conPubs3 As Connection 
 Dim conLoop As Connection 
 
 ' Create ODBCDirect Workspace object. 
 Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Open Connection object using supplied information in 
 ' the connect string. If this information were 
 ' insufficient, you could trap for an error rather than 
 ' go to an ODBC Driver Manager dialog box. 
 MsgBox "Opening Connection1..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Connection1", _ 
 dbDriverNoPrompt, , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Connection object based on information 
 ' you enter in the ODBC Driver Manager dialog box. 
 MsgBox "Opening Connection2..." 
 Set conPubs2 = wrkODBC.OpenConnection("Connection2", _ 
 dbDriverPrompt, True, "ODBC;DSN=Publishers;") 
 
 ' Open read-only Connection object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening Connection3..." 
 Set conPubs3 = wrkODBC.OpenConnection("Connection3", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Connections collection. 
 For Each conLoop In wrkODBC.Connections 
 Debug.Print "Connection properties for " & _ 
 conLoop.Name & ":" 
 
 With conLoop 
 ' Print property values by explicitly calling each 
 ' Property object; the Connection object does not 
 ' support a Properties collection. 
 Debug.Print " Connect = " & .Connect 
 ' Property actually returns a Database object. 
 Debug.Print " Database[.Name] = " & _ 
 .Database.Name 
 Debug.Print " Name = " & .Name 
 Debug.Print " QueryTimeout = " & .QueryTimeout 
 Debug.Print " RecordsAffected = " & _ 
 .RecordsAffected 
 Debug.Print " StillExecuting = " & _ 
 .StillExecuting 
 Debug.Print " Transactions = " & .Transactions 
 Debug.Print " Updatable = " & .Updatable 
 End With 
 
 Next conLoop 
 
 conPubs.Close 
 conPubs2.Close 
 conPubs3.Close 
 wrkODBC.Close 
 
End Sub 
 
```

<br/>

この例では、Microsoft Access **Database** オブジェクトを開いて **Connection** オブジェクトと **Connections** コレクション、および 2 つの ODBCDirect **Connection** オブジェクトの例を示し、各オブジェクトで使用できるプロパティの一覧を示します。

```vb 
Sub ConnectionObjectX() 
 
 Dim wrkAcc as Workspace 
 Dim dbsNorthwind As Database 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim conPubs2 As Connection 
 Dim conLoop As Connection 
 Dim prpLoop As Property 
 
 ' Open Microsoft Access Database object. 
 Set wrkAcc = CreateWorkspace("NewWorkspace", _ 
 "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' objects. 
 Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSNs referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Connection1", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set conPubs2 = wrkODBC.OpenConnection("Connection2", , _ 
 True, "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Debug.Print "Database properties:" 
 
 With dbsNorthwind 
 ' Enumerate Properties collection of Database object. 
 For Each prpLoop In .Properties 
 On Error Resume Next 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop.Value 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 
 ' Enumerate the Connections collection. 
 For Each conLoop In wrkODBC.Connections 
 Debug.Print "Connection properties for " & _ 
 conLoop.Name & ":" 
 
 With conLoop 
 ' Print property values by explicitly calling each 
 ' Property object; the Connection object does not 
 ' support a Properties collection. 
 Debug.Print " Connect = " & .Connect 
 ' Property actually returns a Database object. 
 Debug.Print " Database[.Name] = " & _ 
 .Database.Name 
 Debug.Print " Name = " & .Name 
 Debug.Print " QueryTimeout = " & .QueryTimeout 
 Debug.Print " RecordsAffected = " & _ 
 .RecordsAffected 
 Debug.Print " StillExecuting = " & _ 
 .StillExecuting 
 Debug.Print " Transactions = " & .Transactions 
 Debug.Print " Updatable = " & .Updatable 
 End With 
 
 Next conLoop 
 
 dbsNorthwind.Close 
 conPubs.Close 
 conPubs2.Close 
 wrkAcc.Close 
 wrkODBC.Close 
 
End Sub 
 
```

