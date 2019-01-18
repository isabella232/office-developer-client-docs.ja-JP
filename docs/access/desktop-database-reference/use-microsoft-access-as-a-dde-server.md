---
title: Microsoft Access を DDE サーバーとして使う
TOCTitle: Use Microsoft Access as a DDE Server
description: Access は、DDE 先 (クライアント) アプリケーションまたは DDE 元 (サーバー) アプリケーションとして、Dynamic Data Exchange (DDE) 機能をサポートします。
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0750bdce0e1cda383c48f9c16e62e00997fdfb0a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716377"
---
# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="daa3b-103">Microsoft Access を DDE サーバーとして使う</span><span class="sxs-lookup"><span data-stu-id="daa3b-103">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="daa3b-104">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="daa3b-104">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="daa3b-p101">Access は、DDE 先 (クライアント) アプリケーションまたは DDE 元 (サーバー) アプリケーションとして、Dynamic Data Exchange (DDE) 機能をサポートします。たとえば、クライアントとして動作する Word などのアプリケーションは、サーバーとして動作する Access データベースからのデータを DDE を通じて要求できます。</span><span class="sxs-lookup"><span data-stu-id="daa3b-p101">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application. For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="daa3b-107">[!ヒント] 他のアプリケーションから Access のオブジェクトを操作する必要がある場合は、オートメーションを使うこともできます。</span><span class="sxs-lookup"><span data-stu-id="daa3b-107">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="daa3b-108">クライアントとサーバーの間で DDE 変換を行う場合は、特定のトピックを指定します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-108">A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="daa3b-109">トピックとなるのは、サーバー アプリケーションがサポートする形式のデータ ファイルか、またはサーバー アプリケーション自体の情報を与える System トピックです。</span><span class="sxs-lookup"><span data-stu-id="daa3b-109">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="daa3b-110">特定のトピックについての会話の開始後は、そのトピックに関連付けられているデータ項目だけを転送できます。</span><span class="sxs-lookup"><span data-stu-id="daa3b-110">After a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>

<span data-ttu-id="daa3b-p103">たとえば、Word を実行中に Access のデータベースに含まれるデータを Word 文書に挿入する場合は、 **DDEInitiate** 関数で DDE チャネルを開き、データベースのファイル名をトピックに指定します。これで、データベースから Word へ、チャネルを通じてデータを送信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="daa3b-p103">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document. You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic. You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="daa3b-114">Access を DDE サーバーとして使う場合は、以下のトピックがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="daa3b-114">As a DDE server, Microsoft Access supports the following topics:</span></span>

- <span data-ttu-id="daa3b-115">System トピック</span><span class="sxs-lookup"><span data-stu-id="daa3b-115">The System topic</span></span>

- <span data-ttu-id="daa3b-116">データベース名 (*database* トピック)</span><span class="sxs-lookup"><span data-stu-id="daa3b-116">The name of a database (*database* topic)</span></span>

- <span data-ttu-id="daa3b-117">テーブル名 (*tablename* トピック)</span><span class="sxs-lookup"><span data-stu-id="daa3b-117">The name of a table (*tablename* topic)</span></span>

- <span data-ttu-id="daa3b-118">クエリ名 (*queryname* トピック)</span><span class="sxs-lookup"><span data-stu-id="daa3b-118">The name of a query (*queryname* topic)</span></span>

- <span data-ttu-id="daa3b-119">Access の SQL ステートメント (*sqlstring* トピック)</span><span class="sxs-lookup"><span data-stu-id="daa3b-119">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="daa3b-120">DDE 通信を確立した後は、クライアントからサーバー アプリケーションにコマンドを送信する**DDEExecute**ステートメントを使ってことができます。</span><span class="sxs-lookup"><span data-stu-id="daa3b-120">After you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="daa3b-121">Access を DDE サーバーとして使う場合は、次の内容が有効なコマンドとして認識されます。</span><span class="sxs-lookup"><span data-stu-id="daa3b-121">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

- <span data-ttu-id="daa3b-122">カレント データベースのマクロの名前。</span><span class="sxs-lookup"><span data-stu-id="daa3b-122">The name of a macro in the current database.</span></span>

- <span data-ttu-id="daa3b-123">**DoCmd** オブジェクトの 1 つを使って、Visual Basic で実行できるアクション。</span><span class="sxs-lookup"><span data-stu-id="daa3b-123">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

- <span data-ttu-id="daa3b-p105">DDE 操作でのみ使用される OpenDatabase アクションおよび CloseDatabase アクション。使用法については、このトピックの後の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="daa3b-p105">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations. (For an example of how to use these actions, see the example later in this topic.)</span></span>

> [!NOTE]
> <span data-ttu-id="daa3b-p106">[!メモ] マクロのアクションを **DDEExecute** ステートメントとして指定するときは、 **DoCmd** オブジェクトの構文に従い、アクション名と引数は、角かっこ ([ ]) で囲む必要があります。ただし、DDE を通じて操作されるアプリケーションは、組み込み定数を認識しません。また、引数の文字列にカンマが含まれている場合は、その文字列を二重引用符 ("") で囲む必要があります。カンマが含まれない文字列は、二重引用符で囲む必要はありません。</span><span class="sxs-lookup"><span data-stu-id="daa3b-p106">When you specify a macro action as a **DDEExecute** statement, the action and any arguments follow the **DoCmd** object syntax and must be enclosed in brackets ([ ]). However, applications that support DDE don't recognize intrinsic constants in DDE operations. Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma. Otherwise, quotation marks aren't required.</span></span>

<span data-ttu-id="daa3b-130">クライアント アプリケーションは、 **DDERequest** 関数を使って、開いている DDE チャネルを通じてサーバー アプリケーションにテキスト データを要求できます。</span><span class="sxs-lookup"><span data-stu-id="daa3b-130">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="daa3b-131">または、 **DDEPoke** ステートメントを使って、サーバー アプリケーションにデータを送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="daa3b-131">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="daa3b-132">データ転送の完了後、クライアントは、DDE チャネルを終了するのには、 **DDETerminate**ステートメントまたは**DDETerminateAll**ステートメントをすべての開いているチャネルを閉じるを使用できます。</span><span class="sxs-lookup"><span data-stu-id="daa3b-132">After the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>

> [!NOTE]
> <span data-ttu-id="daa3b-133">[!メモ] クライアント アプリケーションで DDE チャネルを通じてデータを受信した後は、メモリ資源を浪費しないように、DDE チャネルを閉じてください。</span><span class="sxs-lookup"><span data-stu-id="daa3b-133">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span>

<span data-ttu-id="daa3b-p108">次の使用例では、Access を DDE サーバーとして使う Word のプロシージャを、Visual Basic で作成しています。この例を実行するには、Access が実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="daa3b-p108">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server. (For this example to work, Microsoft Access must be running.)</span></span>

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

<br/>

<span data-ttu-id="daa3b-136">次の「System トピック」では、Access がサポートする DDE トピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-136">The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="daa3b-137">System トピック</span><span class="sxs-lookup"><span data-stu-id="daa3b-137">The System topic</span></span>

<span data-ttu-id="daa3b-138">システム トピックは、Microsoft のすべての Windows ベース アプリケーションの標準的なトピックです。</span><span class="sxs-lookup"><span data-stu-id="daa3b-138">The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="daa3b-139">アプリケーションでサポートされているその他のトピックに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-139">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="daa3b-140">この情報にアクセスするに、コードは、*トピック*の引数では、 **DDEInitiate**関数を呼び出して、最初と、引数*item*に指定された次のいずれかで、 **DDERequest**ステートメントを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="daa3b-140">To access this information, your code must first call the **DDEInitiate** function with the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="daa3b-141">アイテム</span><span class="sxs-lookup"><span data-stu-id="daa3b-141">Item</span></span></p></th>
<th><p><span data-ttu-id="daa3b-142">返される値</span><span class="sxs-lookup"><span data-stu-id="daa3b-142">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-143">SysItems</span><span class="sxs-lookup"><span data-stu-id="daa3b-143">SysItems</span></span></p></td>
<td><p><span data-ttu-id="daa3b-144">Access で System トピックがサポートするアイテムの一覧です。</span><span class="sxs-lookup"><span data-stu-id="daa3b-144">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-145">Formats</span><span class="sxs-lookup"><span data-stu-id="daa3b-145">Formats</span></span></p></td>
<td><p><span data-ttu-id="daa3b-146">Access がクリップボードにコピーできる形式の一覧です。</span><span class="sxs-lookup"><span data-stu-id="daa3b-146">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-147">Status</span><span class="sxs-lookup"><span data-stu-id="daa3b-147">Status</span></span></p></td>
<td><p><span data-ttu-id="daa3b-148">&quot;ビジー状態である&quot;または&quot;準備ができた&quot;。</span><span class="sxs-lookup"><span data-stu-id="daa3b-148">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-149">Topics</span><span class="sxs-lookup"><span data-stu-id="daa3b-149">Topics</span></span></p></td>
<td><p><span data-ttu-id="daa3b-150">開いているデータベースの一覧です。</span><span class="sxs-lookup"><span data-stu-id="daa3b-150">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="daa3b-151">次の使用例では、 **DDEInitiate** 関数に System トピックを指定し、 **DDERequest** ステートメントを実行しています。</span><span class="sxs-lookup"><span data-stu-id="daa3b-151">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

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

## <a name="the-database-topic"></a><span data-ttu-id="daa3b-152">データベース トピック</span><span class="sxs-lookup"><span data-stu-id="daa3b-152">The database topic</span></span>

<span data-ttu-id="daa3b-153">*データベース*トピックは、既存のデータベースのファイル名です。</span><span class="sxs-lookup"><span data-stu-id="daa3b-153">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="daa3b-154">基本通り (Northwind)、またはそのパスおよび .mdb ファイルの拡張子のいずれかを入力することができます (c:\\アクセス\\のサンプル\\Northwind.mdb)。</span><span class="sxs-lookup"><span data-stu-id="daa3b-154">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="daa3b-155">データベースとの DDE 通信を開始すると、そのデータベース内のオブジェクトのリストを要求できます。</span><span class="sxs-lookup"><span data-stu-id="daa3b-155">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>

> [!NOTE]
> <span data-ttu-id="daa3b-156">[!メモ] Access のワークグループ情報ファイルに対するクエリを実行するために DDE を使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="daa3b-156">You can't use DDE to query the Microsoft Access workgroup information file.</span></span>

<span data-ttu-id="daa3b-157">*database* トピックでは、以下のアイテムがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="daa3b-157">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="daa3b-158">アイテム</span><span class="sxs-lookup"><span data-stu-id="daa3b-158">Item</span></span></p></th>
<th><p><span data-ttu-id="daa3b-159">返される値</span><span class="sxs-lookup"><span data-stu-id="daa3b-159">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-160">TableList</span><span class="sxs-lookup"><span data-stu-id="daa3b-160">TableList</span></span></p></td>
<td><p><span data-ttu-id="daa3b-161">テーブルの一覧</span><span class="sxs-lookup"><span data-stu-id="daa3b-161">A list of tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-162">QueryList</span><span class="sxs-lookup"><span data-stu-id="daa3b-162">QueryList</span></span></p></td>
<td><p><span data-ttu-id="daa3b-163">クエリの一覧</span><span class="sxs-lookup"><span data-stu-id="daa3b-163">A list of queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-164">FormList</span><span class="sxs-lookup"><span data-stu-id="daa3b-164">FormList</span></span></p></td>
<td><p><span data-ttu-id="daa3b-165">フォームの一覧</span><span class="sxs-lookup"><span data-stu-id="daa3b-165">A list of forms</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-166">ReportList</span><span class="sxs-lookup"><span data-stu-id="daa3b-166">ReportList</span></span></p></td>
<td><p><span data-ttu-id="daa3b-167">レポートの一覧</span><span class="sxs-lookup"><span data-stu-id="daa3b-167">A list of reports</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-168">MacroList</span><span class="sxs-lookup"><span data-stu-id="daa3b-168">MacroList</span></span></p></td>
<td><p><span data-ttu-id="daa3b-169">マクロの一覧</span><span class="sxs-lookup"><span data-stu-id="daa3b-169">A list of macros</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-170">ModuleList</span><span class="sxs-lookup"><span data-stu-id="daa3b-170">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="daa3b-171">モジュールのリスト</span><span class="sxs-lookup"><span data-stu-id="daa3b-171">A list of modules</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-172">ViewList</span><span class="sxs-lookup"><span data-stu-id="daa3b-172">ViewList</span></span></p></td>
<td><p><span data-ttu-id="daa3b-173">ビューの一覧</span><span class="sxs-lookup"><span data-stu-id="daa3b-173">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-174">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="daa3b-174">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="daa3b-175">ストアド プロシージャの一覧</span><span class="sxs-lookup"><span data-stu-id="daa3b-175">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-176">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="daa3b-176">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="daa3b-177">データベース ダイアグラムの一覧</span><span class="sxs-lookup"><span data-stu-id="daa3b-177">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="daa3b-178">次の使用例では、Visual Basic のプロシージャで、ノースウィンド データベースの [社員] フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="daa3b-178">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

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

## <a name="the-table-topic"></a><span data-ttu-id="daa3b-179">テーブル トピック</span><span class="sxs-lookup"><span data-stu-id="daa3b-179">The TABLE topic</span></span>

<span data-ttu-id="daa3b-180">これらのトピックの構文は、以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="daa3b-180">These topics use the following syntax:</span></span>

<span data-ttu-id="daa3b-181">_データベース名_です。**テーブル**_テーブル名_</span><span class="sxs-lookup"><span data-stu-id="daa3b-181">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="daa3b-182">_データベース名_です。**クエリ**_queryname_</span><span class="sxs-lookup"><span data-stu-id="daa3b-182">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="daa3b-183">_データベース名_です。**SQL**[ _sqlstring_ ]</span><span class="sxs-lookup"><span data-stu-id="daa3b-183">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="daa3b-184">指定項目</span><span class="sxs-lookup"><span data-stu-id="daa3b-184">Part</span></span></p></th>
<th><p><span data-ttu-id="daa3b-185">説明</span><span class="sxs-lookup"><span data-stu-id="daa3b-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-186"><em>databasename</em></span><span class="sxs-lookup"><span data-stu-id="daa3b-186"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="daa3b-p111">テーブルやクエリが含まれるデータベース、または SQL ステートメントを適用するデータベースの名前で、末尾にセミコロン (;) を付けます。データベース名の拡張子は省略できます (たとえば Northwind)。または、フル パス名と拡張子を指定することもできます (たとえば C:\\Access\Samples\Northwind.mdb)。</span><span class="sxs-lookup"><span data-stu-id="daa3b-p111">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;). The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-189"><em>tablename</em></span><span class="sxs-lookup"><span data-stu-id="daa3b-189"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="daa3b-190">既存のテーブルの名前です。</span><span class="sxs-lookup"><span data-stu-id="daa3b-190">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-191"><em>queryname</em></span><span class="sxs-lookup"><span data-stu-id="daa3b-191"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="daa3b-192">既存のクエリの名前です。</span><span class="sxs-lookup"><span data-stu-id="daa3b-192">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-193"><em>sqlstring</em></span><span class="sxs-lookup"><span data-stu-id="daa3b-193"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="daa3b-p112">最大 256 文字までの SQL ステートメントで、末尾にセミコロンを付けます。256 文字を超えるステートメントの場合は、この引数を省略し、代わりに連続した <strong>DDEPoke</strong> ステートメントを使って SQL ステートメントを記述します。 たとえば、次の Visual Basic では、 <strong>DDEPoke</strong> ステートメントを使って SQL ステートメントを記述し、クエリの結果を要求しています。  </span><span class="sxs-lookup"><span data-stu-id="daa3b-p112">A valid SQL statement up to 256 characters long, ending with a semicolon. To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement. For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="daa3b-197">次の表に、TABLE *tablename、* QUERY *queryname*、および SQL *sqlstring* の各トピックで使用できるアイテムを示します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-197">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="daa3b-198">アイテム</span><span class="sxs-lookup"><span data-stu-id="daa3b-198">Item</span></span></p></th>
<th><p><span data-ttu-id="daa3b-199">返される値</span><span class="sxs-lookup"><span data-stu-id="daa3b-199">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-200">All</span><span class="sxs-lookup"><span data-stu-id="daa3b-200">All</span></span></p></td>
<td><p><span data-ttu-id="daa3b-201">テーブルに含まれるすべてのデータを、フィールド名も含めて返します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-201">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-202">Data</span><span class="sxs-lookup"><span data-stu-id="daa3b-202">Data</span></span></p></td>
<td><p><span data-ttu-id="daa3b-203">すべての行のデータを返しますが、フィールド名は含まれません。</span><span class="sxs-lookup"><span data-stu-id="daa3b-203">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-204">FieldNames</span><span class="sxs-lookup"><span data-stu-id="daa3b-204">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="daa3b-205">このフィールド名で指定される行を返します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-205">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-206">フィールド名です。T</span><span class="sxs-lookup"><span data-stu-id="daa3b-206">FieldNames;T</span></span></p></td>
<td><p><span data-ttu-id="daa3b-207">1 行目がフィールド名、2 行目がそのデータ型の 2 行を返します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-207">A two-row list of field names (first row) and their data types (second row).</span></span></p>
<p><span data-ttu-id="daa3b-208">これらは、返される値です。</span><span class="sxs-lookup"><span data-stu-id="daa3b-208">These are the values returned:</span></span></p>
<p><span data-ttu-id="daa3b-209">値</span><span class="sxs-lookup"><span data-stu-id="daa3b-209">Value</span></span></p>
<p><ul>
<li><span data-ttu-id="daa3b-210">0</span><span class="sxs-lookup"><span data-stu-id="daa3b-210">0</span></span></li>
<li><span data-ttu-id="daa3b-211">1</span><span class="sxs-lookup"><span data-stu-id="daa3b-211">1</span></span></li>
<li><span data-ttu-id="daa3b-212">2</span><span class="sxs-lookup"><span data-stu-id="daa3b-212">2</span></span></li>
<li><span data-ttu-id="daa3b-213">3</span><span class="sxs-lookup"><span data-stu-id="daa3b-213">3</span></span></li>
<li><span data-ttu-id="daa3b-214">4</span><span class="sxs-lookup"><span data-stu-id="daa3b-214">4</span></span></li>
<li><span data-ttu-id="daa3b-215">5</span><span class="sxs-lookup"><span data-stu-id="daa3b-215">5</span></span></li>
<li><span data-ttu-id="daa3b-216">6</span><span class="sxs-lookup"><span data-stu-id="daa3b-216">6</span></span></li>
<li><span data-ttu-id="daa3b-217">7</span><span class="sxs-lookup"><span data-stu-id="daa3b-217">7</span></span></li>
<li><span data-ttu-id="daa3b-218">8</span><span class="sxs-lookup"><span data-stu-id="daa3b-218">8</span></span></li>
<li><span data-ttu-id="daa3b-219">9</span><span class="sxs-lookup"><span data-stu-id="daa3b-219">9</span></span></li>
<li><span data-ttu-id="daa3b-220">10</span><span class="sxs-lookup"><span data-stu-id="daa3b-220">10</span></span></li>
<li><span data-ttu-id="daa3b-221">11</span><span class="sxs-lookup"><span data-stu-id="daa3b-221">11</span></span></li>
<li><span data-ttu-id="daa3b-222">12</span><span class="sxs-lookup"><span data-stu-id="daa3b-222">12</span></span></li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-223">Nextrow を指定</span><span class="sxs-lookup"><span data-stu-id="daa3b-223">NextRow</span></span></p></td>
<td><p><span data-ttu-id="daa3b-p113">テーブルまたはクエリの現在の行の次の行のデータを返します。チャネルを開いた時点では、NextRow を指定すると最初の行のデータが返されます。現在の行が最終行のときに NextRow を指定すると、要求は失敗します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-p113">The data in the next row in the table or query. When you open a channel, NextRow returns the data in the first row. If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-227">Prevrow を指定します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-227">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="daa3b-p114">テーブルまたはクエリの現在の行の前の行のデータを返します。チャネルを開いた時点では、PrevRow を指定すると最終行のデータが返されます。現在の行が最初の行のときに PrevRow を指定すると、要求は失敗します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-p114">The data in the previous row in the table or query. If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned. If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-231">FirstRow</span><span class="sxs-lookup"><span data-stu-id="daa3b-231">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="daa3b-232">テーブルまたはクエリの最初の行を返します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-232">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-233">LastRow</span><span class="sxs-lookup"><span data-stu-id="daa3b-233">LastRow</span></span></p></td>
<td><p><span data-ttu-id="daa3b-234">テーブルまたはクエリの最後の行を返します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-234">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-235">FieldCount</span><span class="sxs-lookup"><span data-stu-id="daa3b-235">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="daa3b-236">テーブルまたはクエリのフィールドの総数を返します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-236">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa3b-237">SQLText</span><span class="sxs-lookup"><span data-stu-id="daa3b-237">SQLText</span></span></p></td>
<td><p><span data-ttu-id="daa3b-238">テーブルまたはクエリを示す SQL ステートメントです。</span><span class="sxs-lookup"><span data-stu-id="daa3b-238">An SQL statement representing the table or query.</span></span> <span data-ttu-id="daa3b-239">テーブルは、この項目はフォームで、SQL ステートメントを返します&quot;選択`*`<em>テーブル</em>です。&quot;.</span><span class="sxs-lookup"><span data-stu-id="daa3b-239">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa3b-240">SQLText;<em>n</em></span><span class="sxs-lookup"><span data-stu-id="daa3b-240">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="daa3b-241"><em>N</em>で、SQL ステートメントの文字のチャンクは、テーブルまたはクエリは、 <em>n</em>は最大 256 の整数を表します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-241">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="daa3b-242">たとえば、クエリは、次の SQL ステートメントで表される: 項目&quot;SQLText; 7&quot; ] タブで区切られた次のチャンクを取得: アイテム&quot;SQLText; 7&quot; ] タブで区切られた次のチャンクを返します。</span><span class="sxs-lookup"><span data-stu-id="daa3b-242">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="daa3b-243">次の使用例では、Visual Basic プロシージャで DDE を使い、ノースウィンド データベースのテーブルのデータを要求して、そのデータをテキスト ファイルに挿入しています。</span><span class="sxs-lookup"><span data-stu-id="daa3b-243">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

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
