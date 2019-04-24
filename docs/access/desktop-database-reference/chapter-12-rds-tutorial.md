---
title: '12章: リモートデータサービス (RDS) チュートリアル'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aca77ac08688e643327bdbf229ab6c1dec40d109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296480"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a>12章: リモートデータサービス (RDS) チュートリアル

**適用先:** Access 2013、Office 2013

このチュートリアルでは、RDS プログラミング モデルを使用してデータ ソースのクエリおよび更新を行う方法について説明します。 最初に、このタスクの実行に必要な手順を説明します。 このチュートリアルは、microsoft visual Basic Scripting Edition と microsoft visual J++ でも使用されています。これは、Windows Foundation Classes (ado/WFC) 用の ado を特徴としています。

このチュートリアルは、次の 2 つの理由から、複数の言語でコーディングされています。

- RDS の文書は、Visual Basic でのコーディングを前提にしています。そのため、Visual Basic のプログラマには便利ですが、他の言語を使用するプログラマには不便な場合があります。

- RDS の特定の機能についてわからない場合に、他の言語について多少の知識があれば、他の言語で記述された同じ機能を参照することによって問題を解決できる可能性があります。

このチュートリアルは、RDS プログラミング モデルに基づいています。プログラミング モデルの各手順を 1 つずつ説明します。さらに、それぞれの手順に Visual Basic コードの一部を示してあります。

他の言語についても、コード例を最小限の説明と共に取り上げています。各プログラム言語のチュートリアルの手順には、プログラミング モデルとチュートリアルの説明にある手順に対応する番号が付いています。この手順番号を利用して、対応するチュートリアルの説明を参照してください。

RDS プログラミング モデルについて、次に説明します。チュートリアルを使用するうえでのガイドラインとして使用してください。

### <a name="rds-programming-model-with-objects"></a>RDS プログラミング モデルとオブジェクト

- サーバーで呼び出されるプログラムを指定し、クライアントからそのプログラムを参照するための経路 (プロキシ) を取得します。

- サーバー プログラムを呼び出します。データ ソースおよび発行するコマンドを識別するためのパラメーターをサーバー プログラムに渡します。

- サーバー プログラムは、データ ソースから [Recordset](recordset-object-ado.md) オブジェクトを取得します。通常は ADO を使用して取得します。また、サーバー上で **Recordset** オブジェクトを処理することもできます。

- サーバー プログラムは、結果の **Recordset** オブジェクトをクライアント アプリケーションに返します。

- クライアント側では、ビジュアル コントロールを使用すると、必要に応じてフォームに **Recordset** オブジェクトを簡単に配置できます。

- **Recordset** オブジェクトに加えられた変更がサーバーに送り返され、その変更がデータ ソースに反映されます。

## <a name="step-1-specify-a-server-program"></a>手順 1: サーバープログラムを指定する

In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object). サーバープログラムはサーバー上でインスタンス化され、サーバープログラム (*プロキシ*) への参照が返されます。

このチュートリアルでは、既定のサーバー プログラムを使用します。

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a>手順 2: サーバープログラムを呼び出す 

クライアントの "プロキシ" でメソッドを呼び出すと、サーバー上の実際のプログラムでメソッドが実行されます。この手順では、サーバー上でクエリを実行します。

### <a name="part-a"></a>パート A

このチュートリアルで rdsserver.datafactory を使用して[い](datafactory-object-rdsserver.md)ない場合は、この手順を実行する最も便利な方法は、RDS を使用することです[。DataControl](datacontrol-object-rds.md)オブジェクト。 **RDS.DataControl** によって、プロキシを作成する前の手順が、クエリを発行するこの手順と結合されます。

1. RDS を設定し**ます。DataControl**オブジェクト[サーバー](server-property-rds.md)のプロパティを使用して、サーバープログラムをインスタンス化する場所を識別します。

2. [connect](connect-property-rds.md)プロパティを設定して、データソースにアクセスするための接続文字列を指定します。

3. [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado)プロパティを設定して、クエリコマンドテキストを指定します。 

4. サーバープログラムがデータソースに接続し、クエリで指定された行を取得し、 **Recordset**オブジェクトをクライアントに返すようにするには、 [Refresh](refresh-method-rds.md)メソッドを実行します。

このチュートリアルでは **RDS.DataControl** を使用しませんが、使用する場合は次のようになります。

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<br/>

また、このチュートリアルでは ADO オブジェクトを使用して RDS を呼び出しませんが、呼び出す場合は次のようになります。

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a>パート B

この手順を実行するための一般的な方法は、 **rdsserver.datafactory**オブジェクトの[Query](query-method-rds.md)メソッドを呼び出すことです。 このメソッドは、データ ソースへの接続に使用される接続文字列と、データ ソースから返される行の指定に使用されるコマンド テキストを取得します。

このチュートリアルでは、 **DataFactory** オブジェクトの **Query** メソッドを使用します。

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a>手順 3: サーバーが Recordset を取得する 

サーバー プログラムは、目的の行のデータ ソースのクエリを実行するために、接続文字列とコマンド テキストを使用します。通常、この **Recordset** の取得には ADO が使用されますが、マイクロソフトのその他のデータ アクセス インターフェイス (OLE DB など) を使用することもできます。

カスタマー サーバー プログラムは次のようになります。

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a>手順 4: サーバーが Recordset を返す 

RDS は、取得した**recordset**オブジェクトを、クライアントに送り返すことができるフォームに変換します (つまり、 **recordset**を*マーシャリング*します)。 The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library. However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.

クライアント側では、 **Recordset** オブジェクトが返され、ローカル変数に割り当てられます。

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a>手順 5: DataControl を使用できるようにする 

返された **Recordset** オブジェクトは、利用可能な状態です。他の **Recordset** と同様に、調査、移動、または編集を行うことができます。 **Recordset** に対して実行できる操作は、環境によって異なります。Visual Basic および Visual C++ には、直接的に、またはデータ コントロールを使って間接的に **Recordset** を使用できる、ビジュアル コントロールがあります。

たとえば、Internet Explorer で web ページを表示している場合は、ビジュアルコントロールに**Recordset**オブジェクトのデータを表示することができます。 web ページ上のビジュアルコントロールは、 **Recordset**オブジェクトに直接アクセスできません。 しかし、 **DataControl (RDS)** を通じて [Recordset](datacontrol-object-rds.md) にアクセスすることはできます。 **RDS.DataControl** は、その [SourceRecordset](recordset-sourcerecordset-properties-rds.md) プロパティが **Recordset** オブジェクトに設定されている場合に、ビジュアル コントロールによって使用可能な状態になります。

ビジュアル コントロール オブジェクトの **DATASRC** パラメーターは **RDS.DataControl** に、 **DATAFLD** プロパティは **Recordset** オブジェクトのフィールド (列) に設定されている必要があります。

このチュートリアルでは、 **SourceRecordset** プロパティを設定します。

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

## <a name="step-6-changes-are-sent-to-the-server"></a>手順 6: サーバーに変更が送信される

**Recordset** オブジェクトが編集された場合、あらゆる変更内容 (つまり、追加、変更、または削除された行) をサーバーに返送できます。

[!メモ] ADO オブジェクトおよび Microsoft OLE DB Remoting Provider を使用して、RDS の既定の動作を暗黙的に呼び出すことができます。 クエリは**recordset**を返すことができ、編集された**recordset**はデータソースを更新できます。 このチュートリアルでは ADO オブジェクトを使用して RDS を呼び出しませんが、呼び出す場合は次のようになります。

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a>パート A

この場合、RDS のみを使用していると仮定し[ます。DataControl](datacontrol-object-rds.md)を使用して、 **Recordset**オブジェクトが RDS に関連付けられるようになりました **。DataControl**。 [Server](submitchanges-method-rds.md) プロパティと **Connect** プロパティが引き続き設定されていれば、 [SubmitChanges](server-property-rds.md) メソッドによって [Recordset](connect-property-rds.md) オブジェクトへの変更がデータ ソースに反映されます。

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

### <a name="part-b"></a>パート B

または、connection オブジェクトと**Recordset**オブジェクトを指定して、 [rdsserver.datafactory](datafactory-object-rdsserver.md)オブジェクトを使用してサーバーを更新することもできます。

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```


## <a name="appendix-a-rds-tutorial-vbscript"></a>付録 a: RDS チュートリアル (VBScript)

これは、Microsoft Visual Basic Scripting Edition で記述された RDS チュートリアルです。 このチュートリアルの目的の説明については、このトピックの概要を参照してください。

このチュートリアルでは、 [RDS を示します。DataControl](datacontrol-object-rds.md)および[RDS。](dataspace-object-rds.md)デザイン時には、スペースが作成されます。つまり、オブジェクトタグを使用して定義されます。 また、実行時に **Server.CreateObject** メソッドを使用して作成することもできます。 

たとえば、 **RDS.DataControl** オブジェクトは次のようにして作成できます。

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

### <a name="step-1-specify-a-server-program"></a>手順 1: サーバープログラムを指定する

vbscript は、vbscript 要求にアクセスすることによって、実行されている IIS web サーバーの名前を検出できます **。 servervariables**メソッドは、アクティブなサーバーページで使用できます。

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

ただし、このチュートリアルでは、仮想サーバー "the server" を使用します。

> [!NOTE]
> [!メモ] **ByRef** 引数のデータ型に注意してください。VBScript では変数の型指定はできないため、常にバリアント型 (Variant) を渡す必要があります。HTTP を使用している場合は、RDS によってバリアント型 (Variant) をメソッドに渡すことができます。これを **RDS.DataSpace** オブジェクトの [CreateObject](createobject-method-rds.md) メソッドで呼び出すと、非バリアント型となります。DCOM またはインプロセス サーバーを使用している場合は、クライアント側とサーバー側のパラメーター型を一致させてください。一致しない場合は、"型が一致しません。" エラーが発生します。

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a>手順2、パート A: RDS を使用してサーバープログラムを起動します。DataControl

次の例は、 **RDS.DataControl** の既定の動作が指定されたクエリの実行であることを単に示したものです。

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

次の手順に進みます。

### <a name="step-4-server-returns-the-recordset"></a>手順 4: サーバーが Recordset を返す

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a>手順 5: ビジュアルコントロールが DataControl を使用できるようにする

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a>手順6パート A: 変更は、RDS を使用してサーバーに送信されます。DataControl

次の例は、 **RDS.DataControl** がどのようにして更新を行うかを単に示したものです。

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a>手順6パート B: 変更は、rdsserver.datafactory を使用してサーバーに送信されます。 DataFactory

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a>付録 B: RDS チュートリアル (Visual J++)

ADO/WFC は、[DataControl (RDS)](datacontrol-object-rds.md) オブジェクトを実装していないという点で、RDS オブジェクト モデルに完全には準拠していません。ADO/WFC は、クライアント側のクラスの [DataSpace (RDS)](dataspace-object-rds.md) のみを実装しています。

**DataSpace** クラスは、 [ObjectProxy](createobject-method-rds.md) オブジェクトを返す [CreateObject](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) メソッドを実装しています。 **DataSpace** クラスは、 [InternetTimeout](internettimeout-property-rds.md) プロパティも実装しています。

**ObjectProxy** クラスは、サーバー側の任意のビジネス オブジェクトを呼び出すことができる call メソッドを実装しています。

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```



