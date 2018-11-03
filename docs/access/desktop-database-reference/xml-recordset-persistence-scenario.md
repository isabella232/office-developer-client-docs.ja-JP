---
title: XML レコード セットを保存するシナリオ
TOCTitle: XML Recordset persistence scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4840b59f8f145b17b45a9732443d3f844b336868
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945489"
---
# <a name="xml-recordset-persistence-scenario"></a>XML レコード セットを保存するシナリオ

**適用されます**Access 2013、Office 2013。

このシナリオでは、 **Response** オブジェクトの内容を Active Server Pages (ASP) の **Response** オブジェクトに直接保存する ASP アプリケーションを作成します。

> [!NOTE]
> [!メモ] このシナリオを作成するには、サーバーに Internet Information Server 5.0 (IIS) 以降がインストールされている必要があります。

返される **Recordset** は、 [RDS.DataControl](datacontrol-object-rds.md) を使用して Internet Explorer に表示されます。

このシナリオを作成するために必要な手順は次のとおりです。

1.  アプリケーションを設定します。
2.  データを取得します。
3.  データを送信します。
4.  データを受信し、表示します。

## <a name="step-1-set-up-the-application"></a>手順 1: アプリケーションを設定します。

1. **XMLPersist**をという名前のスクリプトのアクセス許可を持つ IIS 仮想ディレクトリを作成します。 

2. フォルダーを仮想ディレクトリが指す、1 つの名前付き**XMLResponse.asp**、およびその他の**Default.htm**に 2 つの新しいテキスト ファイルを作成します。


## <a name="step-2-get-the-data"></a>手順 2: データを取得します。

この手順では、ADO の **Recordset** を開いてクライアントに送信する準備を行うコードを記述します。 

1. Windows のメモ帳などのテキスト エディターで XMLResponse.asp ファイルを開き、次のコードを挿入します。

   ```vb 
        
        <%@ language="VBScript" %> 
        
        <!-- #include file='adovbs.inc' --> 
        
        <% 
        Dim strSQL, strCon 
        Dim adoRec  
        Dim adoCon  
        Dim xmlDoc  
        
        ' You will need to change "slqServer" below to the name of the SQL  
        ' server machine to which you want to connect. 
        strCon = "Provider=sqloledb;Data Source=sqlServer;Initial Catalog=Pubs;Integrated Security=SSPI;" 
        Set adoCon = server.createObject("ADODB.Connection") 
        adoCon.Open strCon 
        
        strSQL = "SELECT Title, Price FROM Titles ORDER BY Price" 
        Set adoRec = Server.CreateObject("ADODB.Recordset") 
        adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText 
   ```

2. StrCon でデータ ソースのパラメーターの値を Microsoft SQL Server コンピューターの名前に変更することを確認します。

3. ファイルを開いたままで、次の手順に進みます。

## <a name="step-3-send-the-data"></a>手順 3: データを送信します。

**Recordset** の準備が完了したので、これを XML として ASP **Response** オブジェクトに保存して、クライアントに送信する必要があります。 

1. XMLResponse.asp の最後に次のコードを追加します。

   ```vb 
    
    Response.ContentType = "text/xml" 
    Response.Expires = 0 
    Response.Buffer = False 
    
    
    Response.Write "<?xml version='1.0'?>" & vbNewLine 
    adoRec.save Response, adPersistXML 
    adoRec.Close 
    Set adoRec=Nothing 
    %> 
   ```

   ASP**応答**オブジェクトが**レコード セット**の[保存](save-method-ado.md)メソッドの保存先として指定されていることを確認します。 **Save** メソッドの保存先には、 **IStream** インターフェイスをサポートする任意のオブジェクト (ADO の [Stream](stream-object-ado.md) オブジェクトなど)、または、 **Recordset** の保存先の完全なパスを含むファイル名を指定できます。

2. XMLResponse.asp を保存して閉じ、次の手順に進みます。 Adovbs.inc ファイルを c: からコピーも\\Program Files\\ファイルの一般的な\\システム\\XMLResponse.asp ファイルがあるフォルダーにフォルダーを Ado。

## <a name="step-4-receive-and-display-the-data"></a>手順 4: が受信し、データを表示

この手順では、埋め込みの[rds. で HTML ファイルを作成しますDataControl](datacontrol-object-rds.md)オブジェクトを**レコード セット**を得るための XMLResponse.asp ファイルをポイントします。 

1. Windows メモ帳などのテキスト エディターで default.htm を開き、次のコードを追加します。 URL の "sqlserver" は、実際に使用するサーバー コンピューターの名前に置き換えてください。

   ```html 
    
    <HTML> 
    <HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
    <BODY> 
    
    <TABLE DATASRC="#RDC1" border="1"> 
    <TR> 
    <TD><SPAN DATAFLD="title"></SPAN></TD> 
    <TD><SPAN DATAFLD="price"></SPAN></TD> 
    </TR> 
    </TABLE> 

    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
    <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
    </OBJECT> 
    
    </BODY> 
    </HTML> 
   ```

2. Default.htm ファイルを閉じ、XMLResponse.asp を保存した同じフォルダーに保存します。 

3. Internet Explorer 4.0 を使用して、後で、URL を開くまたは`https://<sqlserver>/XMLPersist/default.htm`し、結果を確認します。 データは、バインドされた DHTML テーブルに表示されます。 

4. URL を開くようになりました`https://<sqlserver>/XMLPersist/XMLResponse.asp`し、結果を確認します。 XML が表示されます。




