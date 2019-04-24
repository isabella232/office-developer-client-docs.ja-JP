---
title: XML レコードセットの永続化シナリオ
TOCTitle: XML Recordset persistence scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5bae48f3e9b2b5c3967b955c41ba01c634546164
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302597"
---
# <a name="xml-recordset-persistence-scenario"></a>XML レコードセットの永続化シナリオ

**適用先:** Access 2013、Office 2013

このシナリオでは、 **Response** オブジェクトの内容を Active Server Pages (ASP) の **Response** オブジェクトに直接保存する ASP アプリケーションを作成します。

> [!NOTE]
> [!メモ] このシナリオを作成するには、サーバーに Internet Information Server 5.0 (IIS) 以降がインストールされている必要があります。

返される **Recordset** は、 [RDS.DataControl](datacontrol-object-rds.md) を使用して Internet Explorer に表示されます。

このシナリオを作成するために必要な手順は次のとおりです。

1.  アプリケーションを設定します。
2.  データを取得します。
3.  データを送信します。
4.  データを受信し、表示します。

## <a name="step-1-set-up-the-application"></a>手順 1: アプリケーションをセットアップする

1. 「スクリプト権限を使用して**xmlpersist** 」という名前の IIS 仮想ディレクトリを作成します。 

2. 仮想ディレクトリをポイントするフォルダーに2つの新しいテキストファイルを作成します。このファイルには、 **xmlresponse**という名前の、もう1つの**default.htm**という名前が付けられます。


## <a name="step-2-get-the-data"></a>手順 2: データを取得する

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

2. 必ず、strcon のデータソースパラメーターの値を Microsoft SQL Server コンピュータの名前に変更してください。

3. ファイルを開いたままで、次の手順に進みます。

## <a name="step-3-send-the-data"></a>手順 3: データを送信する

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

   ASP **Response**オブジェクトは、 **Recordset** [Save](save-method-ado.md)メソッドの宛先として指定されていることに注意してください。 **Save** メソッドの保存先には、 **IStream** インターフェイスをサポートする任意のオブジェクト (ADO の [Stream](stream-object-ado.md) オブジェクトなど)、または、 **Recordset** の保存先の完全なパスを含むファイル名を指定できます。

2. XMLResponse.asp を保存して閉じ、次の手順に進みます。 また、\\adovbs.inc ファイルを C: Program Files\\Common Files\\System\\Ado フォルダーから xmlresponse .asp ファイルと同じフォルダーにコピーします。

## <a name="step-4-receive-and-display-the-data"></a>手順 4: データを受信して表示する

この手順では、埋め込みの RDS を含む HTML ファイルを作成し[ます。](datacontrol-object-rds.md) **Recordset**を取得するために xmlresponse .asp ファイルをポイントする DataControl オブジェクト。 

1. Windows メモ帳などのテキストエディターを使用して default.htm を開き、次のコードを追加します。 URL の "sqlserver" は、実際に使用するサーバー コンピューターの名前に置き換えてください。

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

2. Close the default.htm file and save it to the same folder where you saved XMLResponse.asp. 

3. Internet Explorer 4.0 以降を使用して、URL `https://<sqlserver>/XMLPersist/default.htm`を開き、結果を確認します。 The data is displayed in a bound DHTML table. 

4. 次に、URL `https://<sqlserver>/XMLPersist/XMLResponse.asp`を開いて結果を確認します。 The XML is displayed.




