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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313392"
---
# <a name="use-microsoft-access-as-a-dde-server"></a>Microsoft Access を DDE サーバーとして使う

**適用先:** Access 2013、Office 2013 

Access は、DDE 先 (クライアント) アプリケーションまたは DDE 元 (サーバー) アプリケーションとして、Dynamic Data Exchange (DDE) 機能をサポートします。たとえば、クライアントとして動作する Word などのアプリケーションは、サーバーとして動作する Access データベースからのデータを DDE を通じて要求できます。

> [!TIP]
> [!ヒント] 他のアプリケーションから Access のオブジェクトを操作する必要がある場合は、オートメーションを使うこともできます。

クライアントとサーバーの間で DDE 変換を行う場合は、特定のトピックを指定します。 トピックとなるのは、サーバー アプリケーションがサポートする形式のデータ ファイルか、またはサーバー アプリケーション自体の情報を与える System トピックです。 特定のトピックで会話が開始されると、そのトピックに関連付けられているデータ項目のみが転送されます。

たとえば、Word を実行中に Access のデータベースに含まれるデータを Word 文書に挿入する場合は、 **DDEInitiate** 関数で DDE チャネルを開き、データベースのファイル名をトピックに指定します。これで、データベースから Word へ、チャネルを通じてデータを送信できるようになります。

Access を DDE サーバーとして使う場合は、以下のトピックがサポートされます。

- System トピック

- データベース名 (*database* トピック)

- テーブル名 (*tablename* トピック)

- クエリ名 (*queryname* トピック)

- Access の SQL ステートメント (*sqlstring* トピック)

DDE 会話を確立したら、 **DDEExecute**ステートメントを使用して、クライアントからサーバーアプリケーションにコマンドを送信できます。 Access を DDE サーバーとして使う場合は、次の内容が有効なコマンドとして認識されます。

- カレント データベースのマクロの名前。

- **DoCmd** オブジェクトの 1 つを使って、Visual Basic で実行できるアクション。

- DDE 操作でのみ使用される OpenDatabase アクションおよび CloseDatabase アクション。使用法については、このトピックの後の例を参照してください。

> [!NOTE]
> [!メモ] マクロのアクションを **DDEExecute** ステートメントとして指定するときは、 **DoCmd** オブジェクトの構文に従い、アクション名と引数は、角かっこ ([ ]) で囲む必要があります。ただし、DDE を通じて操作されるアプリケーションは、組み込み定数を認識しません。また、引数の文字列にカンマが含まれている場合は、その文字列を二重引用符 ("") で囲む必要があります。カンマが含まれない文字列は、二重引用符で囲む必要はありません。

クライアント アプリケーションは、 **DDERequest** 関数を使って、開いている DDE チャネルを通じてサーバー アプリケーションにテキスト データを要求できます。 または、 **DDEPoke** ステートメントを使って、サーバー アプリケーションにデータを送信することもできます。 データ転送の完了後、クライアントは**DDETerminate**ステートメントを使用して DDE チャネルを閉じるか、 **DDETerminateAll**ステートメントを使用して、開いているすべてのチャネルを閉じることができます。

> [!NOTE]
> [!メモ] クライアント アプリケーションで DDE チャネルを通じてデータを受信した後は、メモリ資源を浪費しないように、DDE チャネルを閉じてください。

次の使用例では、Access を DDE サーバーとして使う Word のプロシージャを、Visual Basic で作成しています。この例を実行するには、Access が実行されている必要があります。

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

次の「System トピック」では、Access がサポートする DDE トピックについて説明します。

## <a name="the-system-topic"></a>System トピック

System トピックは、すべての Windows 対応アプリケーションで使用できる標準的なトピックです。 このトピックは、そのアプリケーションでサポートされるトピックに関する情報を返します。 この情報にアクセスするには、最初に*topic*引数を指定して**DDEInitiate**関数を呼び出し、次に*item*引数に次のいずれかを指定して**DDERequest**ステートメントを実行する必要があります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Item</p></th>
<th><p>戻り値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>sysitems</p></td>
<td><p>Access で System トピックがサポートするアイテムの一覧です。</p></td>
</tr>
<tr class="even">
<td><p>Formats</p></td>
<td><p>Access がクリップボードにコピーできる形式の一覧です。</p></td>
</tr>
<tr class="odd">
<td><p>Status</p></td>
<td><p>&quot;取り込み&quot;中&quot;また&quot;は準備中です。</p></td>
</tr>
<tr class="even">
<td><p>Topics</p></td>
<td><p>開いているデータベースの一覧です。</p></td>
</tr>
</tbody>
</table>

<br/>

次の使用例では、 **DDEInitiate** 関数に System トピックを指定し、 **DDERequest** ステートメントを実行しています。

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

## <a name="the-database-topic"></a>データベーストピック

*database*トピックは、既存のデータベースのファイル名です。 基本的な名前 (northwind) だけを入力することも、そのパスと .mdb の拡張子 (C:\\Access\\の\\サンプル northwind.mdb) を入力することもできます。 After you start a DDE conversation with the database, you can request a list of the objects in that database.

> [!NOTE]
> [!メモ] Access のワークグループ情報ファイルに対するクエリを実行するために DDE を使うことはできません。

*database* トピックでは、以下のアイテムがサポートされます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Item</p></th>
<th><p>戻り値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>tablelist</p></td>
<td><p>テーブルのリスト</p></td>
</tr>
<tr class="even">
<td><p>querylist</p></td>
<td><p>クエリの一覧</p></td>
</tr>
<tr class="odd">
<td><p>formlist</p></td>
<td><p>フォームの一覧</p></td>
</tr>
<tr class="even">
<td><p>ReportList</p></td>
<td><p>レポートの一覧</p></td>
</tr>
<tr class="odd">
<td><p>マクロリスト</p></td>
<td><p>マクロの一覧</p></td>
</tr>
<tr class="even">
<td><p>modulelist</p></td>
<td><p>モジュールの一覧</p></td>
</tr>
<tr class="odd">
<td><p>ViewList</p></td>
<td><p>ビューの一覧</p></td>
</tr>
<tr class="even">
<td><p>StoredProcedureList</p></td>
<td><p>ストアド プロシージャの一覧</p></td>
</tr>
<tr class="odd">
<td><p>databaseダイアグラムのリスト</p></td>
<td><p>データベース ダイアグラムの一覧</p></td>
</tr>
</tbody>
</table>

<br/>

次の使用例では、Visual Basic のプロシージャで、ノースウィンド データベースの [社員] フォームを開きます。

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

## <a name="the-table-topic"></a>表のトピック

これらのトピックの構文は、以下のとおりです。

_databasename_ ;**表**_tablename_

_databasename_ ;**クエリ**_queryname_

_databasename_ ;**SQL**[ _sqlstring_ ]

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パーツ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>databasename</em></p></td>
<td><p>The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;). The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</p></td>
</tr>
<tr class="even">
<td><p><em>tablename</em></p></td>
<td><p>既存のテーブルの名前です。</p></td>
</tr>
<tr class="odd">
<td><p><em>queryname</em></p></td>
<td><p>既存のクエリの名前です。</p></td>
</tr>
<tr class="even">
<td><p><em>sqlstring</em></p></td>
<td><p>最大 256 文字までの SQL ステートメントで、末尾にセミコロンを付けます。256 文字を超えるステートメントの場合は、この引数を省略し、代わりに連続した <strong>DDEPoke</strong> ステートメントを使って SQL ステートメントを記述します。 たとえば、次の Visual Basic では、 <strong>DDEPoke</strong> ステートメントを使って SQL ステートメントを記述し、クエリの結果を要求しています。  </p></td>
</tr>
</tbody>
</table>

<br/>

次の表に、TABLE *tablename、* QUERY *queryname*、および SQL *sqlstring* の各トピックで使用できるアイテムを示します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Item</p></th>
<th><p>戻り値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>All</p></td>
<td><p>テーブルに含まれるすべてのデータを、フィールド名も含めて返します。</p></td>
</tr>
<tr class="even">
<td><p>Data</p></td>
<td><p>すべての行のデータを返しますが、フィールド名は含まれません。</p></td>
</tr>
<tr class="odd">
<td><p>FieldNames</p></td>
<td><p>このフィールド名で指定される行を返します。</p></td>
</tr>
<tr class="even">
<td><p>FieldNamesなく</p></td>
<td><p>1 行目がフィールド名、2 行目がそのデータ型の 2 行を返します。</p>
<p>返される値は次のとおりです。</p>
<p>値</p>
<p><ul>
<li>.0</li>
<li>1-d</li>
<li>pbm-2</li>
<li>1/3</li>
<li>2/4</li>
<li>5</li>
<li>シックス</li>
<li>7</li>
<li>~</li>
<li>i-9</li>
<li>個</li>
<li>#</li>
<li>個</li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p>NextRow</p></td>
<td><p>テーブルまたはクエリの現在の行の次の行のデータを返します。チャネルを開いた時点では、NextRow を指定すると最初の行のデータが返されます。現在の行が最終行のときに NextRow を指定すると、要求は失敗します。</p></td>
</tr>
<tr class="odd">
<td><p>PrevRow</p></td>
<td><p>テーブルまたはクエリの現在の行の前の行のデータを返します。チャネルを開いた時点では、PrevRow を指定すると最終行のデータが返されます。現在の行が最初の行のときに PrevRow を指定すると、要求は失敗します。</p></td>
</tr>
<tr class="even">
<td><p>FirstRow</p></td>
<td><p>テーブルまたはクエリの最初の行を返します。</p></td>
</tr>
<tr class="odd">
<td><p>LastRow</p></td>
<td><p>テーブルまたはクエリの最後の行を返します。</p></td>
</tr>
<tr class="even">
<td><p>fieldcount</p></td>
<td><p>テーブルまたはクエリのフィールドの総数を返します。</p></td>
</tr>
<tr class="odd">
<td><p>SQLText</p></td>
<td><p>テーブルまたはクエリを示す SQL ステートメントです。 テーブルの場合、このアイテムはフォーム&quot;の選択`*` <em>テーブル</em>で SQL ステートメントを返します。&quot;.</p></td>
</tr>
<tr class="even">
<td><p>SQLText;<em>n</em></p></td>
<td><p><em>n</em>文字のチャンクで構成される SQL ステートメント。 n は、テーブルまたはクエリを表します。ここで、 <em>n</em>は256までの整数です。 たとえば、クエリが次の SQL ステートメントで表されているとします&quot;。アイテム SQLText&quot; ; 7 は、次のタブで区切られ&quot;たチャンクを&quot;返します。 item SQLText; 7 は、次のタブで区切られたチャンクを返します。</p></td>
</tr>
</tbody>
</table>

<br/>

次の使用例では、Visual Basic プロシージャで DDE を使い、ノースウィンド データベースのテーブルのデータを要求して、そのデータをテキスト ファイルに挿入しています。

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
