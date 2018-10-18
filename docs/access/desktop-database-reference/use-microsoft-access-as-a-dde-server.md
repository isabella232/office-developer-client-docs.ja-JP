---
<span data-ttu-id="de68d-101">タイトル: TOCTitle DDE サーバーとして使用されます DDE サーバーとして Microsoft Access を使用して <<<<<<< ヘッド ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: 48546801 ms.date: 2015/09/18 ===。説明: Microsoft Access は、送信先 (クライアント) アプリケーションまたはソース (サーバー) アプリケーションとしてダイナミック データ エクス (チェンジ DDE) をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="de68d-101">title: Use Microsoft Access as a DDE server TOCTitle: Use Microsoft Access as a DDE Server <<<<<<< HEAD ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: 48546801 ms.date: 09/18/2015 ======= description: Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application.</span></span>  
<span data-ttu-id="de68d-102">ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: 48546801 ms.date: 2018/10/16</span><span class="sxs-lookup"><span data-stu-id="de68d-102">ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: 48546801 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="de68d-103">マスター mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="de68d-103">master mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="de68d-104">vbaac10.chm5186349 f1_categories。</span><span class="sxs-lookup"><span data-stu-id="de68d-104">vbaac10.chm5186349 f1_categories:</span></span>
- <span data-ttu-id="de68d-105">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="de68d-105">Office.Version=v15</span></span>
---

# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="de68d-106">Access を DDE サーバーとして使用します。</span><span class="sxs-lookup"><span data-stu-id="de68d-106">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="de68d-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="de68d-107">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="de68d-p101">Access は、DDE 先 (クライアント) アプリケーションまたは DDE 元 (サーバー) アプリケーションとして、Dynamic Data Exchange (DDE) 機能をサポートします。たとえば、クライアントとして動作する Word などのアプリケーションは、サーバーとして動作する Access データベースからのデータを DDE を通じて要求できます。</span><span class="sxs-lookup"><span data-stu-id="de68d-p101">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application. For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="de68d-110">[!ヒント] 他のアプリケーションから Access のオブジェクトを操作する必要がある場合は、オートメーションを使うこともできます。</span><span class="sxs-lookup"><span data-stu-id="de68d-110">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="de68d-111"><<<<<<< ヘッド A 間の dde クライアントとサーバーが特定のトピックを確立します。</span><span class="sxs-lookup"><span data-stu-id="de68d-111"><<<<<<< HEAD A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="de68d-112">トピックとなるのは、サーバー アプリケーションがサポートする形式のデータ ファイルか、またはサーバー アプリケーション自体の情報を与える System トピックです。</span><span class="sxs-lookup"><span data-stu-id="de68d-112">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="de68d-113">特定のトピックで変換が始まった後は、指定したトピックに関連するデータ アイテムのみが送信されます。</span><span class="sxs-lookup"><span data-stu-id="de68d-113">Once a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>
<span data-ttu-id="de68d-114">=== 特定のトピックでは、クライアントとサーバー間での DDE 通信が確立されます。</span><span class="sxs-lookup"><span data-stu-id="de68d-114">======= A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="de68d-115">トピックとなるのは、サーバー アプリケーションがサポートする形式のデータ ファイルか、またはサーバー アプリケーション自体の情報を与える System トピックです。</span><span class="sxs-lookup"><span data-stu-id="de68d-115">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="de68d-116">特定のトピックについての会話の開始後は、そのトピックに関連付けられているデータ項目だけを転送できます。</span><span class="sxs-lookup"><span data-stu-id="de68d-116">After a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>
>>>>>>> <span data-ttu-id="de68d-117">master</span><span class="sxs-lookup"><span data-stu-id="de68d-117">master</span></span>

<span data-ttu-id="de68d-p103">たとえば、Word を実行中に Access のデータベースに含まれるデータを Word 文書に挿入する場合は、 **DDEInitiate** 関数で DDE チャネルを開き、データベースのファイル名をトピックに指定します。これで、データベースから Word へ、チャネルを通じてデータを送信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="de68d-p103">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document. You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic. You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="de68d-121">Access を DDE サーバーとして使う場合は、以下のトピックがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="de68d-121">As a DDE server, Microsoft Access supports the following topics:</span></span>

<span data-ttu-id="de68d-122"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="de68d-122"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="de68d-123">System トピック</span><span class="sxs-lookup"><span data-stu-id="de68d-123">The System topic</span></span>

  - <span data-ttu-id="de68d-124">データベース名 (*database* トピック)</span><span class="sxs-lookup"><span data-stu-id="de68d-124">The name of a database (*database* topic)</span></span>

  - <span data-ttu-id="de68d-125">テーブル名 (*tablename* トピック)</span><span class="sxs-lookup"><span data-stu-id="de68d-125">The name of a table (*tablename* topic)</span></span>

  - <span data-ttu-id="de68d-126">クエリ名 (*queryname* トピック)</span><span class="sxs-lookup"><span data-stu-id="de68d-126">The name of a query (*queryname* topic)</span></span>

  - <span data-ttu-id="de68d-127">Access の SQL ステートメント (*sqlstring* トピック)</span><span class="sxs-lookup"><span data-stu-id="de68d-127">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="de68d-p104">DDE 変換を実行すると、 **DDEExecute** ステートメントを使って、クライアント アプリケーションからサーバー アプリケーションにコマンドを送信できます。Access を DDE サーバーとして使う場合は、次の内容が有効なコマンドとして認識されます。</span><span class="sxs-lookup"><span data-stu-id="de68d-p104">Once you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application. When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

  - <span data-ttu-id="de68d-130">カレント データベースのマクロの名前。</span><span class="sxs-lookup"><span data-stu-id="de68d-130">The name of a macro in the current database.</span></span>

  - <span data-ttu-id="de68d-131">**DoCmd** オブジェクトの 1 つを使って、Visual Basic で実行できるアクション。</span><span class="sxs-lookup"><span data-stu-id="de68d-131">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

  - <span data-ttu-id="de68d-p105">DDE 操作でのみ使用される OpenDatabase アクションおよび CloseDatabase アクション。使用法については、このトピックの後の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de68d-p105">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations. (For an example of how to use these actions, see the example later in this topic.)</span></span>


> [!NOTE]
> <P><span data-ttu-id="de68d-p106">[!メモ] マクロのアクションを <STRONG>DDEExecute</STRONG> ステートメントとして指定するときは、 <STRONG>DoCmd</STRONG> オブジェクトの構文に従い、アクション名と引数は、角かっこ ([ ]) で囲む必要があります。ただし、DDE を通じて操作されるアプリケーションは、組み込み定数を認識しません。また、引数の文字列にカンマが含まれている場合は、その文字列を二重引用符 ("") で囲む必要があります。カンマが含まれない文字列は、二重引用符で囲む必要はありません。</span><span class="sxs-lookup"><span data-stu-id="de68d-p106">When you specify a macro action as a <STRONG>DDEExecute</STRONG> statement, the action and any arguments follow the <STRONG>DoCmd</STRONG> object syntax and must be enclosed in brackets ([ ]). However, applications that support DDE don't recognize intrinsic constants in DDE operations. Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma. Otherwise, quotation marks aren't required.</span></span></P>



<span data-ttu-id="de68d-p107">クライアント アプリケーションは、 **DDERequest** 関数を使って、開いている DDE チャネルを通じてサーバー アプリケーションにテキスト データを要求できます。または、 **DDEPoke** ステートメントを使って、サーバー アプリケーションにデータを送信することもできます。通信終了後に、クライアントは **DDETerminate** ステートメントで DDE チャネルを閉じるか、または **DDETerminateAll** ステートメントで開いているすべてのチャネルを閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="de68d-p107">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel. Or the client can use the **DDEPoke** statement to send data to the server application. Once the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>


> [!NOTE]
> <P><span data-ttu-id="de68d-141">[!メモ] クライアント アプリケーションで DDE チャネルを通じてデータを受信した後は、メモリ資源を浪費しないように、DDE チャネルを閉じてください。</span><span class="sxs-lookup"><span data-stu-id="de68d-141">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span></P>


=======
- <span data-ttu-id="de68d-142">System トピック</span><span class="sxs-lookup"><span data-stu-id="de68d-142">The System topic</span></span>

- <span data-ttu-id="de68d-143">データベース名 (*database* トピック)</span><span class="sxs-lookup"><span data-stu-id="de68d-143">The name of a database (*database* topic)</span></span>

- <span data-ttu-id="de68d-144">テーブル名 (*tablename* トピック)</span><span class="sxs-lookup"><span data-stu-id="de68d-144">The name of a table (*tablename* topic)</span></span>

- <span data-ttu-id="de68d-145">クエリ名 (*queryname* トピック)</span><span class="sxs-lookup"><span data-stu-id="de68d-145">The name of a query (*queryname* topic)</span></span>

- <span data-ttu-id="de68d-146">Access の SQL ステートメント (*sqlstring* トピック)</span><span class="sxs-lookup"><span data-stu-id="de68d-146">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="de68d-147">DDE 通信を確立した後は、クライアントからサーバー アプリケーションにコマンドを送信する**DDEExecute**ステートメントを使ってことができます。</span><span class="sxs-lookup"><span data-stu-id="de68d-147">After you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="de68d-148">Access を DDE サーバーとして使う場合は、次の内容が有効なコマンドとして認識されます。</span><span class="sxs-lookup"><span data-stu-id="de68d-148">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

- <span data-ttu-id="de68d-149">カレント データベースのマクロの名前。</span><span class="sxs-lookup"><span data-stu-id="de68d-149">The name of a macro in the current database.</span></span>

- <span data-ttu-id="de68d-150">**DoCmd** オブジェクトの 1 つを使って、Visual Basic で実行できるアクション。</span><span class="sxs-lookup"><span data-stu-id="de68d-150">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

- <span data-ttu-id="de68d-p109">DDE 操作でのみ使用される OpenDatabase アクションおよび CloseDatabase アクション。使用法については、このトピックの後の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de68d-p109">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations. (For an example of how to use these actions, see the example later in this topic.)</span></span>

> [!NOTE]
> <span data-ttu-id="de68d-p110">[!メモ] マクロのアクションを **DDEExecute** ステートメントとして指定するときは、 **DoCmd** オブジェクトの構文に従い、アクション名と引数は、角かっこ ([ ]) で囲む必要があります。ただし、DDE を通じて操作されるアプリケーションは、組み込み定数を認識しません。また、引数の文字列にカンマが含まれている場合は、その文字列を二重引用符 ("") で囲む必要があります。カンマが含まれない文字列は、二重引用符で囲む必要はありません。</span><span class="sxs-lookup"><span data-stu-id="de68d-p110">When you specify a macro action as a **DDEExecute** statement, the action and any arguments follow the **DoCmd** object syntax and must be enclosed in brackets ([ ]). However, applications that support DDE don't recognize intrinsic constants in DDE operations. Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma. Otherwise, quotation marks aren't required.</span></span>

<span data-ttu-id="de68d-157">クライアント アプリケーションは、 **DDERequest** 関数を使って、開いている DDE チャネルを通じてサーバー アプリケーションにテキスト データを要求できます。</span><span class="sxs-lookup"><span data-stu-id="de68d-157">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="de68d-158">または、 **DDEPoke** ステートメントを使って、サーバー アプリケーションにデータを送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="de68d-158">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="de68d-159">データ転送の完了後、クライアントは、DDE チャネルを終了するのには、 **DDETerminate**ステートメントまたは**DDETerminateAll**ステートメントをすべての開いているチャネルを閉じるを使用できます。</span><span class="sxs-lookup"><span data-stu-id="de68d-159">After the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>

> [!NOTE]
> <span data-ttu-id="de68d-160">[!メモ] クライアント アプリケーションで DDE チャネルを通じてデータを受信した後は、メモリ資源を浪費しないように、DDE チャネルを閉じてください。</span><span class="sxs-lookup"><span data-stu-id="de68d-160">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span>
>>>>>>> <span data-ttu-id="de68d-161">master</span><span class="sxs-lookup"><span data-stu-id="de68d-161">master</span></span>

<span data-ttu-id="de68d-p112">次の使用例では、Access を DDE サーバーとして使う Word のプロシージャを、Visual Basic で作成しています。この例を実行するには、Access が実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de68d-p112">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server. (For this example to work, Microsoft Access must be running.)</span></span>

```vb
    Sub AccessDDE() 
        Dim intChan1 As Integer, intChan2 As Integer 
        Dim strQueryData As String 
     
        ' Use System topic to open Northwind sample database. 
        ' Database must be open before using other DDE topics. 
        intChan1 = DDEInitiate("MSAccess", "System") 
        ' You may need to change this path to point to actual location 
        ' of Northwind sample database. 
        DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]" 
     
        ' Get all data from Ten Most Expensive Products query. 
        intChan2 = DDEInitiate("MSAccess", "Northwind.mdb;" _ 
            & "QUERY Ten Most Expensive Products") 
        strQueryData = DDERequest(intChan2, "All") 
        DDETerminate intChan2 
     
        ' Close database. 
        DDEExecute intChan1, "[CloseDatabase]" 
        DDETerminate intChan1 
     
        ' Print retrieved data to Debug Window. 
        Debug.Print strQueryData 
    End Sub
```

<a name="-head"></a><span data-ttu-id="de68d-164"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="de68d-164"><<<<<<< HEAD</span></span>
=======
<br/>

>>>>>>> <span data-ttu-id="de68d-165">マスターは次のセクションでは、Microsoft Access でサポートされている有効な DDE トピックに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="de68d-165">master The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="de68d-166">System トピック</span><span class="sxs-lookup"><span data-stu-id="de68d-166">The System topic</span></span>

<span data-ttu-id="de68d-167"><<<<<<< ヘッドの「システムのトピックでは、すべて Microsoft Windows ベース アプリケーションの標準的なトピックです。</span><span class="sxs-lookup"><span data-stu-id="de68d-167"><<<<<<< HEAD The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="de68d-168">アプリケーションでサポートされているその他のトピックに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="de68d-168">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="de68d-169">この情報にアクセスするには、コードする必要があります最初に*トピック*の引数として、 **DDEInitiate**関数を呼び出すし、引数*item*に指定された次のいずれかで、 **DDERequest**ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="de68d-169">To access this information, your code must first call the **DDEInitiate** function with as the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>
<span data-ttu-id="de68d-170">=== システム トピックは、Microsoft のすべての Windows ベース アプリケーションの標準的なトピックです。</span><span class="sxs-lookup"><span data-stu-id="de68d-170">======= The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="de68d-171">アプリケーションでサポートされているその他のトピックに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="de68d-171">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="de68d-172">この情報にアクセスするに、コードは、*トピック*の引数では、 **DDEInitiate**関数を呼び出して、最初と、引数*item*に指定された次のいずれかで、 **DDERequest**ステートメントを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de68d-172">To access this information, your code must first call the **DDEInitiate** function with the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>
>>>>>>> <span data-ttu-id="de68d-173">master</span><span class="sxs-lookup"><span data-stu-id="de68d-173">master</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de68d-174">アイテム</span><span class="sxs-lookup"><span data-stu-id="de68d-174">Item</span></span></p></th>
<th><p><span data-ttu-id="de68d-175">返される値</span><span class="sxs-lookup"><span data-stu-id="de68d-175">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de68d-176">SysItems</span><span class="sxs-lookup"><span data-stu-id="de68d-176">SysItems</span></span></p></td>
<td><p><span data-ttu-id="de68d-177">Access で System トピックがサポートするアイテムの一覧です。</span><span class="sxs-lookup"><span data-stu-id="de68d-177">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-178">Formats</span><span class="sxs-lookup"><span data-stu-id="de68d-178">Formats</span></span></p></td>
<td><p><span data-ttu-id="de68d-179">Access がクリップボードにコピーできる形式の一覧です。</span><span class="sxs-lookup"><span data-stu-id="de68d-179">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de68d-180">Status</span><span class="sxs-lookup"><span data-stu-id="de68d-180">Status</span></span></p></td>
<td><p><span data-ttu-id="de68d-181">&quot;ビジー状態である&quot;または&quot;準備ができた&quot;。</span><span class="sxs-lookup"><span data-stu-id="de68d-181">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-182">Topics</span><span class="sxs-lookup"><span data-stu-id="de68d-182">Topics</span></span></p></td>
<td><p><span data-ttu-id="de68d-183">開いているデータベースの一覧です。</span><span class="sxs-lookup"><span data-stu-id="de68d-183">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><span data-ttu-id="de68d-184"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="de68d-184"><<<<<<< HEAD</span></span>
=======
<br/>
>>>>>>> <span data-ttu-id="de68d-185">master</span><span class="sxs-lookup"><span data-stu-id="de68d-185">master</span></span>

<span data-ttu-id="de68d-186">次の使用例では、 **DDEInitiate** 関数に System トピックを指定し、 **DDERequest** ステートメントを実行しています。</span><span class="sxs-lookup"><span data-stu-id="de68d-186">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

```vb
    ' In Visual Basic, initiate DDE conversation with Microsoft Access. 
    Dim intChan1 As Integer, strResults As String 
    intChan1 = DDEInitiate("MSAccess", "System") 
    ' Request list of topics supported by System topic. 
    strResults = DDERequest(intChan1, "SysItems") 
    ' Run OpenDatabase action to open Northwind.mdb. 
    ' You may need to change this path to point to actual location 
    ' of Northwind sample database. 
    DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]"
```

## <a name="the-database-topic"></a><span data-ttu-id="de68d-187">データベース トピック</span><span class="sxs-lookup"><span data-stu-id="de68d-187">The database topic</span></span>

<span data-ttu-id="de68d-188">*データベース*トピックは、既存のデータベースのファイル名です。</span><span class="sxs-lookup"><span data-stu-id="de68d-188">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="de68d-189">基本通り (Northwind)、またはそのパスおよび .mdb ファイルの拡張子のいずれかを入力することができます (c:\\アクセス\\のサンプル\\Northwind.mdb)。</span><span class="sxs-lookup"><span data-stu-id="de68d-189">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="de68d-190">データベースとの DDE 通信を開始すると、そのデータベース内のオブジェクトのリストを要求できます。</span><span class="sxs-lookup"><span data-stu-id="de68d-190">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>

<span data-ttu-id="de68d-191"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="de68d-191"><<<<<<< HEAD</span></span>

> [!NOTE]
> <P><span data-ttu-id="de68d-192">[!メモ] Access のワークグループ情報ファイルに対するクエリを実行するために DDE を使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="de68d-192">You can't use DDE to query the Microsoft Access workgroup information file.</span></span></P>


=======
> [!NOTE]
> <span data-ttu-id="de68d-193">[!メモ] Access のワークグループ情報ファイルに対するクエリを実行するために DDE を使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="de68d-193">You can't use DDE to query the Microsoft Access workgroup information file.</span></span>
>>>>>>> <span data-ttu-id="de68d-194">master</span><span class="sxs-lookup"><span data-stu-id="de68d-194">master</span></span>

<span data-ttu-id="de68d-195">*database* トピックでは、以下のアイテムがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="de68d-195">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de68d-196">アイテム</span><span class="sxs-lookup"><span data-stu-id="de68d-196">Item</span></span></p></th>
<th><p><span data-ttu-id="de68d-197">返される値</span><span class="sxs-lookup"><span data-stu-id="de68d-197">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de68d-198">TableList</span><span class="sxs-lookup"><span data-stu-id="de68d-198">TableList</span></span></p></td>
<span data-ttu-id="de68d-199"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="de68d-199"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="de68d-200">テーブルの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-200">A list of tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-201">QueryList</span><span class="sxs-lookup"><span data-stu-id="de68d-201">QueryList</span></span></p></td>
<td><p><span data-ttu-id="de68d-202">クエリの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-202">A list of queries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de68d-203">FormList</span><span class="sxs-lookup"><span data-stu-id="de68d-203">FormList</span></span></p></td>
<td><p><span data-ttu-id="de68d-204">フォームの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-204">A list of forms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-205">ReportList</span><span class="sxs-lookup"><span data-stu-id="de68d-205">ReportList</span></span></p></td>
<td><p><span data-ttu-id="de68d-206">レポートの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-206">A list of reports.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de68d-207">MacroList</span><span class="sxs-lookup"><span data-stu-id="de68d-207">MacroList</span></span></p></td>
<td><p><span data-ttu-id="de68d-208">マクロの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-208">A list of macros.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-209">ModuleList</span><span class="sxs-lookup"><span data-stu-id="de68d-209">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="de68d-210">モジュールの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-210">A list of modules.</span></span></p></td>
=======
<td><p><span data-ttu-id="de68d-211">テーブルの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-211">A list of tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-212">QueryList</span><span class="sxs-lookup"><span data-stu-id="de68d-212">QueryList</span></span></p></td>
<td><p><span data-ttu-id="de68d-213">クエリの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-213">A list of queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de68d-214">FormList</span><span class="sxs-lookup"><span data-stu-id="de68d-214">FormList</span></span></p></td>
<td><p><span data-ttu-id="de68d-215">フォームの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-215">A list of forms</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-216">ReportList</span><span class="sxs-lookup"><span data-stu-id="de68d-216">ReportList</span></span></p></td>
<td><p><span data-ttu-id="de68d-217">レポートの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-217">A list of reports</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de68d-218">MacroList</span><span class="sxs-lookup"><span data-stu-id="de68d-218">MacroList</span></span></p></td>
<td><p><span data-ttu-id="de68d-219">マクロの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-219">A list of macros</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-220">ModuleList</span><span class="sxs-lookup"><span data-stu-id="de68d-220">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="de68d-221">モジュールのリスト</span><span class="sxs-lookup"><span data-stu-id="de68d-221">A list of modules</span></span></p></td><span data-ttu-id="de68d-222">
>>>>>>>マスター</span><span class="sxs-lookup"><span data-stu-id="de68d-222">
>>>>>>> master</span></span>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de68d-223">ViewList</span><span class="sxs-lookup"><span data-stu-id="de68d-223">ViewList</span></span></p></td>
<td><p><span data-ttu-id="de68d-224">ビューの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-224">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-225">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="de68d-225">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="de68d-226">ストアド プロシージャの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-226">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de68d-227">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="de68d-227">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="de68d-228">データベース ダイアグラムの一覧</span><span class="sxs-lookup"><span data-stu-id="de68d-228">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><span data-ttu-id="de68d-229"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="de68d-229"><<<<<<< HEAD</span></span>
=======
<br/>
>>>>>>> <span data-ttu-id="de68d-230">master</span><span class="sxs-lookup"><span data-stu-id="de68d-230">master</span></span>

<span data-ttu-id="de68d-231">次の使用例では、Visual Basic のプロシージャで、ノースウィンド データベースの [社員] フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="de68d-231">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

```vb
    ' In Visual Basic, initiate DDE conversation with 
    ' Northwind sample database. 
    ' Make sure database is open. 
    intChan2 = DDEInitiate("MSAccess", "Northwind") 
    ' Request list of forms in Northwind sample database. 
    strResponse = DDERequest(intChan2, "FormList") 
    ' Run OpenForm action and arguments to open Employees form. 
    DDEExecute intChan2, "[OpenForm Employees,0,,,1,0]"
```

## <a name="the-table-topic"></a><span data-ttu-id="de68d-232">テーブル トピック</span><span class="sxs-lookup"><span data-stu-id="de68d-232">The TABLE topic</span></span>

<span data-ttu-id="de68d-233">これらのトピックの構文は、以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="de68d-233">These topics use the following syntax:</span></span>

<span data-ttu-id="de68d-234">_データベース名_です。**テーブル**_テーブル名_</span><span class="sxs-lookup"><span data-stu-id="de68d-234">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="de68d-235">_データベース名_です。**クエリ**_queryname_</span><span class="sxs-lookup"><span data-stu-id="de68d-235">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="de68d-236">_データベース名_です。**SQL**[ _sqlstring_ ]</span><span class="sxs-lookup"><span data-stu-id="de68d-236">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de68d-237">パーツ</span><span class="sxs-lookup"><span data-stu-id="de68d-237">Part</span></span></p></th>
<th><p><span data-ttu-id="de68d-238">説明</span><span class="sxs-lookup"><span data-stu-id="de68d-238">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de68d-239"><em>databasename</em></span><span class="sxs-lookup"><span data-stu-id="de68d-239"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="de68d-p115">テーブルやクエリが含まれるデータベース、または SQL ステートメントを適用するデータベースの名前で、末尾にセミコロン (;) を付けます。データベース名の拡張子は省略できます (たとえば Northwind)。または、フル パス名と拡張子を指定することもできます (たとえば C:\\Access\Samples\Northwind.mdb)。</span><span class="sxs-lookup"><span data-stu-id="de68d-p115">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;). The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-242"><em>tablename</em></span><span class="sxs-lookup"><span data-stu-id="de68d-242"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="de68d-243">既存のテーブルの名前です。</span><span class="sxs-lookup"><span data-stu-id="de68d-243">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de68d-244"><em>queryname</em></span><span class="sxs-lookup"><span data-stu-id="de68d-244"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="de68d-245">既存のクエリの名前です。</span><span class="sxs-lookup"><span data-stu-id="de68d-245">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-246"><em>sqlstring</em></span><span class="sxs-lookup"><span data-stu-id="de68d-246"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="de68d-p116">最大 256 文字までの SQL ステートメントで、末尾にセミコロンを付けます。256 文字を超えるステートメントの場合は、この引数を省略し、代わりに連続した <strong>DDEPoke</strong> ステートメントを使って SQL ステートメントを記述します。 たとえば、次の Visual Basic では、 <strong>DDEPoke</strong> ステートメントを使って SQL ステートメントを記述し、クエリの結果を要求しています。  </span><span class="sxs-lookup"><span data-stu-id="de68d-p116">A valid SQL statement up to 256 characters long, ending with a semicolon. To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement. For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="de68d-250">次の表に、TABLE *tablename、* QUERY *queryname*、および SQL *sqlstring* の各トピックで使用できるアイテムを示します。</span><span class="sxs-lookup"><span data-stu-id="de68d-250">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de68d-251">アイテム</span><span class="sxs-lookup"><span data-stu-id="de68d-251">Item</span></span></p></th>
<th><p><span data-ttu-id="de68d-252">返される値</span><span class="sxs-lookup"><span data-stu-id="de68d-252">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de68d-253">All</span><span class="sxs-lookup"><span data-stu-id="de68d-253">All</span></span></p></td>
<td><p><span data-ttu-id="de68d-254">テーブルに含まれるすべてのデータを、フィールド名も含めて返します。</span><span class="sxs-lookup"><span data-stu-id="de68d-254">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-255">Data</span><span class="sxs-lookup"><span data-stu-id="de68d-255">Data</span></span></p></td>
<td><p><span data-ttu-id="de68d-256">すべての行のデータを返しますが、フィールド名は含まれません。</span><span class="sxs-lookup"><span data-stu-id="de68d-256">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de68d-257">FieldNames</span><span class="sxs-lookup"><span data-stu-id="de68d-257">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="de68d-258">このフィールド名で指定される行を返します。</span><span class="sxs-lookup"><span data-stu-id="de68d-258">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-259">フィールド名です。T</span><span class="sxs-lookup"><span data-stu-id="de68d-259">FieldNames;T</span></span></p></td>
<span data-ttu-id="de68d-260"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="de68d-260"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="de68d-261">1 行目がフィールド名、2 行目がそのデータ型の 2 行を返します。</span><span class="sxs-lookup"><span data-stu-id="de68d-261">A two-row list of field names (first row) and their data types (second row).</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-262">返される値とその値が示すデータ型は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="de68d-262">These are the values returned and the data types they represent:</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-263"><b>値</b></span><span class="sxs-lookup"><span data-stu-id="de68d-263"><b>Value</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-264">0</span><span class="sxs-lookup"><span data-stu-id="de68d-264">0</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-265">1</span><span class="sxs-lookup"><span data-stu-id="de68d-265">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-266">2</span><span class="sxs-lookup"><span data-stu-id="de68d-266">2</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-267">3</span><span class="sxs-lookup"><span data-stu-id="de68d-267">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-268">4</span><span class="sxs-lookup"><span data-stu-id="de68d-268">4</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-269">5</span><span class="sxs-lookup"><span data-stu-id="de68d-269">5</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-270">6</span><span class="sxs-lookup"><span data-stu-id="de68d-270">6</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-271">7</span><span class="sxs-lookup"><span data-stu-id="de68d-271">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-272">8</span><span class="sxs-lookup"><span data-stu-id="de68d-272">8</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-273">9</span><span class="sxs-lookup"><span data-stu-id="de68d-273">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-274">10</span><span class="sxs-lookup"><span data-stu-id="de68d-274">10</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-275">11</span><span class="sxs-lookup"><span data-stu-id="de68d-275">11</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="de68d-276">12</span><span class="sxs-lookup"><span data-stu-id="de68d-276">12</span></span></p></td>
=======
<td><p><span data-ttu-id="de68d-277">1 行目がフィールド名、2 行目がそのデータ型の 2 行を返します。</span><span class="sxs-lookup"><span data-stu-id="de68d-277">A two-row list of field names (first row) and their data types (second row).</span></span></p>
<p><span data-ttu-id="de68d-278">これらは、返される値です。</span><span class="sxs-lookup"><span data-stu-id="de68d-278">These are the values returned:</span></span></p>
<p><span data-ttu-id="de68d-279">値</span><span class="sxs-lookup"><span data-stu-id="de68d-279">Value</span></span></p>
<p><ul>
<li><span data-ttu-id="de68d-280">0</span><span class="sxs-lookup"><span data-stu-id="de68d-280">0</span></span></li>
<li><span data-ttu-id="de68d-281">1</span><span class="sxs-lookup"><span data-stu-id="de68d-281">1</span></span></li>
<li><span data-ttu-id="de68d-282">2</span><span class="sxs-lookup"><span data-stu-id="de68d-282">2</span></span></li>
<li><span data-ttu-id="de68d-283">3</span><span class="sxs-lookup"><span data-stu-id="de68d-283">3</span></span></li>
<li><span data-ttu-id="de68d-284">4</span><span class="sxs-lookup"><span data-stu-id="de68d-284">4</span></span></li>
<li><span data-ttu-id="de68d-285">5</span><span class="sxs-lookup"><span data-stu-id="de68d-285">5</span></span></li>
<li><span data-ttu-id="de68d-286">6</span><span class="sxs-lookup"><span data-stu-id="de68d-286">6</span></span></li>
<li><span data-ttu-id="de68d-287">7</span><span class="sxs-lookup"><span data-stu-id="de68d-287">7</span></span></li>
<li><span data-ttu-id="de68d-288">8</span><span class="sxs-lookup"><span data-stu-id="de68d-288">8</span></span></li>
<li><span data-ttu-id="de68d-289">9</span><span class="sxs-lookup"><span data-stu-id="de68d-289">9</span></span></li>
<li><span data-ttu-id="de68d-290">10</span><span class="sxs-lookup"><span data-stu-id="de68d-290">10</span></span></li>
<li><span data-ttu-id="de68d-291">11</span><span class="sxs-lookup"><span data-stu-id="de68d-291">11</span></span></li>
<li><span data-ttu-id="de68d-292">12</span><span class="sxs-lookup"><span data-stu-id="de68d-292">12</span></span></li>
</ul>
</p>
</td><span data-ttu-id="de68d-293">
>>>>>>>マスター</span><span class="sxs-lookup"><span data-stu-id="de68d-293">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-294">Nextrow を指定</span><span class="sxs-lookup"><span data-stu-id="de68d-294">NextRow</span></span></p></td>
<td><p><span data-ttu-id="de68d-p117">テーブルまたはクエリの現在の行の次の行のデータを返します。チャネルを開いた時点では、NextRow を指定すると最初の行のデータが返されます。現在の行が最終行のときに NextRow を指定すると、要求は失敗します。</span><span class="sxs-lookup"><span data-stu-id="de68d-p117">The data in the next row in the table or query. When you open a channel, NextRow returns the data in the first row. If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de68d-298">Prevrow を指定します。</span><span class="sxs-lookup"><span data-stu-id="de68d-298">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="de68d-p118">テーブルまたはクエリの現在の行の前の行のデータを返します。チャネルを開いた時点では、PrevRow を指定すると最終行のデータが返されます。現在の行が最初の行のときに PrevRow を指定すると、要求は失敗します。</span><span class="sxs-lookup"><span data-stu-id="de68d-p118">The data in the previous row in the table or query. If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned. If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-302">FirstRow</span><span class="sxs-lookup"><span data-stu-id="de68d-302">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="de68d-303">テーブルまたはクエリの最初の行を返します。</span><span class="sxs-lookup"><span data-stu-id="de68d-303">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de68d-304">LastRow</span><span class="sxs-lookup"><span data-stu-id="de68d-304">LastRow</span></span></p></td>
<td><p><span data-ttu-id="de68d-305">テーブルまたはクエリの最後の行を返します。</span><span class="sxs-lookup"><span data-stu-id="de68d-305">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-306">FieldCount</span><span class="sxs-lookup"><span data-stu-id="de68d-306">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="de68d-307">テーブルまたはクエリのフィールドの総数を返します。</span><span class="sxs-lookup"><span data-stu-id="de68d-307">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de68d-308">SQLText</span><span class="sxs-lookup"><span data-stu-id="de68d-308">SQLText</span></span></p></td>
<td><p><span data-ttu-id="de68d-309">テーブルまたはクエリを示す SQL ステートメントです。</span><span class="sxs-lookup"><span data-stu-id="de68d-309">An SQL statement representing the table or query.</span></span> <span data-ttu-id="de68d-310">テーブルは、この項目はフォームで、SQL ステートメントを返します&quot;選択`*`<em>テーブル</em>です。&quot;.</span><span class="sxs-lookup"><span data-stu-id="de68d-310">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de68d-311">SQLText;<em>n</em></span><span class="sxs-lookup"><span data-stu-id="de68d-311">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="de68d-312"><em>N</em>で、SQL ステートメントの文字のチャンクは、テーブルまたはクエリは、 <em>n</em>は最大 256 の整数を表します。</span><span class="sxs-lookup"><span data-stu-id="de68d-312">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="de68d-313">たとえば、クエリは、次の SQL ステートメントで表される: 項目&quot;SQLText; 7&quot; ] タブで区切られた次のチャンクを取得: アイテム&quot;SQLText; 7&quot; ] タブで区切られた次のチャンクを返します。</span><span class="sxs-lookup"><span data-stu-id="de68d-313">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><span data-ttu-id="de68d-314"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="de68d-314"><<<<<<< HEAD</span></span>
=======
<br/>
>>>>>>> <span data-ttu-id="de68d-315">master</span><span class="sxs-lookup"><span data-stu-id="de68d-315">master</span></span>

<span data-ttu-id="de68d-316">次の使用例では、Visual Basic プロシージャで DDE を使い、ノースウィンド データベースのテーブルのデータを要求して、そのデータをテキスト ファイルに挿入しています。</span><span class="sxs-lookup"><span data-stu-id="de68d-316">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

```vb
    Sub NorthwindDDE 
        Dim intChan1 As Integer, intChan2 As Integer, intChan3 As Integer 
        Dim strResp1 As Variant, strResp2 As Variant, strResp3 As Variant 
     
        ' In a Visual Basic module, get data from Categories table, 
        ' Catalog query, and Orders table in Northwind.mdb. 
        ' Make sure database is open first. 
        intChan1 = DDEInitiate("MSAccess", "Northwind;TABLE Shippers") 
        intChan2 = DDEInitiate("MSAccess", "Northwind;QUERY Catalog") 
        intChan3 = DDEInitiate("MSAccess", "Northwind;SQL SELECT * " _ 
            & "FROM Orders " _ 
            & "WHERE OrderID > 10050;") 
     
        strResp1 = DDERequest(intChan1, "All") 
        strResp2 = DDERequest(intChan2, "FieldNames;T") 
        strResp3 = DDERequest(intChan3, "FieldNames;T") 
        DDETerminate intChan1 
        DDETerminate intChan2 
        DDETerminate intChan3 
     
        ' Insert data into text file. 
        Open "C:\DATA.TXT" For Append As #1 
        Print #1, strResp1 
        Print #1, strResp2 
        Print #1, strResp3 
        Close #1 
    End Sub
```
