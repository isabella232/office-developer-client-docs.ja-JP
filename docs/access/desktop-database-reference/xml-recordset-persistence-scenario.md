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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711533"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="78027-102">XML レコードセットの永続化シナリオ</span><span class="sxs-lookup"><span data-stu-id="78027-102">XML Recordset persistence scenario</span></span>

<span data-ttu-id="78027-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="78027-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="78027-104">このシナリオでは、 **Response** オブジェクトの内容を Active Server Pages (ASP) の **Response** オブジェクトに直接保存する ASP アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="78027-104">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="78027-105">[!メモ] このシナリオを作成するには、サーバーに Internet Information Server 5.0 (IIS) 以降がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="78027-105">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="78027-106">返される **Recordset** は、 [RDS.DataControl](datacontrol-object-rds.md) を使用して Internet Explorer に表示されます。</span><span class="sxs-lookup"><span data-stu-id="78027-106">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="78027-107">このシナリオを作成するために必要な手順は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="78027-107">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="78027-108">アプリケーションを設定します。</span><span class="sxs-lookup"><span data-stu-id="78027-108">Set up the application.</span></span>
2.  <span data-ttu-id="78027-109">データを取得します。</span><span class="sxs-lookup"><span data-stu-id="78027-109">Get the data.</span></span>
3.  <span data-ttu-id="78027-110">データを送信します。</span><span class="sxs-lookup"><span data-stu-id="78027-110">Send the data.</span></span>
4.  <span data-ttu-id="78027-111">データを受信し、表示します。</span><span class="sxs-lookup"><span data-stu-id="78027-111">Receive and display the data.</span></span>

## <a name="step-1-set-up-the-application"></a><span data-ttu-id="78027-112">手順 1: アプリケーションを設定します。</span><span class="sxs-lookup"><span data-stu-id="78027-112">Step 1: Set up the application</span></span>

1. <span data-ttu-id="78027-113">**XMLPersist**をという名前のスクリプトのアクセス許可を持つ IIS 仮想ディレクトリを作成します。</span><span class="sxs-lookup"><span data-stu-id="78027-113">Create an IIS virtual directory named **XMLPersist** with script permissions.</span></span> 

2. <span data-ttu-id="78027-114">フォルダーを仮想ディレクトリが指す、1 つの名前付き**XMLResponse.asp**、およびその他の**Default.htm**に 2 つの新しいテキスト ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="78027-114">Create two new text files in the folder to which the virtual directory points, one named **XMLResponse.asp**, and the other named **Default.htm**.</span></span>


## <a name="step-2-get-the-data"></a><span data-ttu-id="78027-115">手順 2: データを取得します。</span><span class="sxs-lookup"><span data-stu-id="78027-115">Step 2: Get the data</span></span>

<span data-ttu-id="78027-116">この手順では、ADO の **Recordset** を開いてクライアントに送信する準備を行うコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="78027-116">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client.</span></span> 

1. <span data-ttu-id="78027-117">Windows のメモ帳などのテキスト エディターで XMLResponse.asp ファイルを開き、次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="78027-117">Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

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

2. <span data-ttu-id="78027-118">StrCon でデータ ソースのパラメーターの値を Microsoft SQL Server コンピューターの名前に変更することを確認します。</span><span class="sxs-lookup"><span data-stu-id="78027-118">Be sure to change the value of the Data Source parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

3. <span data-ttu-id="78027-119">ファイルを開いたままで、次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="78027-119">Keep the file open and go on to the next step.</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="78027-120">手順 3: データを送信します。</span><span class="sxs-lookup"><span data-stu-id="78027-120">Step 3: Send the data</span></span>

<span data-ttu-id="78027-121">**Recordset** の準備が完了したので、これを XML として ASP **Response** オブジェクトに保存して、クライアントに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="78027-121">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object.</span></span> 

1. <span data-ttu-id="78027-122">XMLResponse.asp の最後に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="78027-122">Add the following code to the bottom of XMLResponse.asp:</span></span>

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

   <span data-ttu-id="78027-123">ASP**応答**オブジェクトが**レコード セット**の[保存](save-method-ado.md)メソッドの保存先として指定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="78027-123">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="78027-124">**Save** メソッドの保存先には、 **IStream** インターフェイスをサポートする任意のオブジェクト (ADO の [Stream](stream-object-ado.md) オブジェクトなど)、または、 **Recordset** の保存先の完全なパスを含むファイル名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="78027-124">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

2. <span data-ttu-id="78027-125">XMLResponse.asp を保存して閉じ、次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="78027-125">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="78027-126">Adovbs.inc ファイルを c: からコピーも\\Program Files\\ファイルの一般的な\\システム\\XMLResponse.asp ファイルがあるフォルダーにフォルダーを Ado。</span><span class="sxs-lookup"><span data-stu-id="78027-126">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="78027-127">手順 4: が受信し、データを表示</span><span class="sxs-lookup"><span data-stu-id="78027-127">Step 4: Receive and display the data</span></span>

<span data-ttu-id="78027-128">この手順では、埋め込みの[rds. で HTML ファイルを作成しますDataControl](datacontrol-object-rds.md)オブジェクトを**レコード セット**を得るための XMLResponse.asp ファイルをポイントします。</span><span class="sxs-lookup"><span data-stu-id="78027-128">In this step, you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**.</span></span> 

1. <span data-ttu-id="78027-129">Windows メモ帳などのテキスト エディターで default.htm を開き、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="78027-129">Open default.htm with a text editor, such as Windows Notepad, and add the following code.</span></span> <span data-ttu-id="78027-130">URL の "sqlserver" は、実際に使用するサーバー コンピューターの名前に置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="78027-130">Replace "sqlserver" in the URL with the name of your server computer.</span></span>

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

2. <span data-ttu-id="78027-131">Default.htm ファイルを閉じ、XMLResponse.asp を保存した同じフォルダーに保存します。</span><span class="sxs-lookup"><span data-stu-id="78027-131">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> 

3. <span data-ttu-id="78027-132">Internet Explorer 4.0 を使用して、後で、URL を開くまたは`https://<sqlserver>/XMLPersist/default.htm`し、結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="78027-132">Using Internet Explorer 4.0 or later, open the URL `https://<sqlserver>/XMLPersist/default.htm` and observe the results.</span></span> <span data-ttu-id="78027-133">データは、バインドされた DHTML テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="78027-133">The data is displayed in a bound DHTML table.</span></span> 

4. <span data-ttu-id="78027-134">URL を開くようになりました`https://<sqlserver>/XMLPersist/XMLResponse.asp`し、結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="78027-134">Now open the URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` and observe the results.</span></span> <span data-ttu-id="78027-135">XML が表示されます。</span><span class="sxs-lookup"><span data-stu-id="78027-135">The XML is displayed.</span></span>




