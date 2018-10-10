---
title: Access を DDE サーバーとして使用します。
TOCTitle: Use Microsoft Access as a DDE Server
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 84b4e30877488d84e03839764c1996053e76a2e7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478745"
---
# <a name="use-microsoft-access-as-a-dde-server"></a>Access を DDE サーバーとして使用します。

**適用されます**Access 2013 |。Office 2013 

Access は、DDE 先 (クライアント) アプリケーションまたは DDE 元 (サーバー) アプリケーションとして、Dynamic Data Exchange (DDE) 機能をサポートします。たとえば、クライアントとして動作する Word などのアプリケーションは、サーバーとして動作する Access データベースからのデータを DDE を通じて要求できます。

> [!TIP]
> [!ヒント] 他のアプリケーションから Access のオブジェクトを操作する必要がある場合は、オートメーションを使うこともできます。

クライアントとサーバーの間で DDE 変換を行う場合は、特定のトピックを指定します。トピックとなるのは、サーバー アプリケーションがサポートする形式のデータ ファイルか、またはサーバー アプリケーション自体の情報を与える System トピックです。特定のトピックで変換が始まった後は、指定したトピックに関連するデータ アイテムのみが送信されます。

たとえば、Word を実行中に Access のデータベースに含まれるデータを Word 文書に挿入する場合は、 **DDEInitiate** 関数で DDE チャネルを開き、データベースのファイル名をトピックに指定します。これで、データベースから Word へ、チャネルを通じてデータを送信できるようになります。

Access を DDE サーバーとして使う場合は、以下のトピックがサポートされます。

  - System トピック

  - データベース名 (*database* トピック)

  - テーブル名 (*tablename* トピック)

  - クエリ名 (*queryname* トピック)

  - Access の SQL ステートメント (*sqlstring* トピック)

DDE 変換を実行すると、 **DDEExecute** ステートメントを使って、クライアント アプリケーションからサーバー アプリケーションにコマンドを送信できます。Access を DDE サーバーとして使う場合は、次の内容が有効なコマンドとして認識されます。

  - カレント データベースのマクロの名前。

  - **DoCmd** オブジェクトの 1 つを使って、Visual Basic で実行できるアクション。

  - DDE 操作でのみ使用される OpenDatabase アクションおよび CloseDatabase アクション。使用法については、このトピックの後の例を参照してください。


> [!NOTE]
> <P>[!メモ] マクロのアクションを <STRONG>DDEExecute</STRONG> ステートメントとして指定するときは、 <STRONG>DoCmd</STRONG> オブジェクトの構文に従い、アクション名と引数は、角かっこ ([ ]) で囲む必要があります。ただし、DDE を通じて操作されるアプリケーションは、組み込み定数を認識しません。また、引数の文字列にカンマが含まれている場合は、その文字列を二重引用符 ("") で囲む必要があります。カンマが含まれない文字列は、二重引用符で囲む必要はありません。</P>



クライアント アプリケーションは、 **DDERequest** 関数を使って、開いている DDE チャネルを通じてサーバー アプリケーションにテキスト データを要求できます。または、 **DDEPoke** ステートメントを使って、サーバー アプリケーションにデータを送信することもできます。通信終了後に、クライアントは **DDETerminate** ステートメントで DDE チャネルを閉じるか、または **DDETerminateAll** ステートメントで開いているすべてのチャネルを閉じることができます。


> [!NOTE]
> <P>[!メモ] クライアント アプリケーションで DDE チャネルを通じてデータを受信した後は、メモリ資源を浪費しないように、DDE チャネルを閉じてください。</P>



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

次の「System トピック」では、Access がサポートする DDE トピックについて説明します。

## <a name="the-system-topic"></a>System トピック

システム トピックは、Microsoft のすべての Windows ベース アプリケーションの標準的なトピックです。 アプリケーションでサポートされているその他のトピックに関する情報を提供します。 この情報にアクセスするには、コードする必要があります最初に*トピック*の引数として、 **DDEInitiate**関数を呼び出すし、引数*item*に指定された次のいずれかで、 **DDERequest**ステートメントを実行します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アイテム</p></th>
<th><p>返される値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SysItems</p></td>
<td><p>Access で System トピックがサポートするアイテムの一覧です。</p></td>
</tr>
<tr class="even">
<td><p>Formats</p></td>
<td><p>Access がクリップボードにコピーできる形式の一覧です。</p></td>
</tr>
<tr class="odd">
<td><p>Status</p></td>
<td><p>&quot;ビジー状態である&quot;または&quot;準備ができた&quot;。</p></td>
</tr>
<tr class="even">
<td><p>Topics</p></td>
<td><p>開いているデータベースの一覧です。</p></td>
</tr>
</tbody>
</table>


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

## <a name="the-database-topic"></a>データベース トピック

*データベース*トピックは、既存のデータベースのファイル名です。 基本通り (Northwind)、またはそのパスおよび .mdb ファイルの拡張子のいずれかを入力することができます (c:\\アクセス\\のサンプル\\Northwind.mdb)。 データベースとの DDE 通信を開始すると、そのデータベース内のオブジェクトのリストを要求できます。


> [!NOTE]
> <P>[!メモ] Access のワークグループ情報ファイルに対するクエリを実行するために DDE を使うことはできません。</P>



*database* トピックでは、以下のアイテムがサポートされます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アイテム</p></th>
<th><p>返される値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TableList</p></td>
<td><p>テーブルの一覧</p></td>
</tr>
<tr class="even">
<td><p>QueryList</p></td>
<td><p>クエリの一覧</p></td>
</tr>
<tr class="odd">
<td><p>FormList</p></td>
<td><p>フォームの一覧</p></td>
</tr>
<tr class="even">
<td><p>ReportList</p></td>
<td><p>レポートの一覧</p></td>
</tr>
<tr class="odd">
<td><p>MacroList</p></td>
<td><p>マクロの一覧</p></td>
</tr>
<tr class="even">
<td><p>ModuleList</p></td>
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
<td><p>DatabaseDiagramList</p></td>
<td><p>データベース ダイアグラムの一覧</p></td>
</tr>
</tbody>
</table>


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

## <a name="the-table-topic"></a>テーブル トピック

これらのトピックの構文は、以下のとおりです。

_データベース名_です。**テーブル**_テーブル名_

_データベース名_です。**クエリ**_queryname_

_データベース名_です。**SQL**[ _sqlstring_ ]

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
<td><p>テーブルやクエリが含まれるデータベース、または SQL ステートメントを適用するデータベースの名前で、末尾にセミコロン (;) を付けます。データベース名の拡張子は省略できます (たとえば Northwind)。または、フル パス名と拡張子を指定することもできます (たとえば C:\\Access\Samples\Northwind.mdb)。</p></td>
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
<th><p>アイテム</p></th>
<th><p>返される値</p></th>
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
<td><p>フィールド名です。T</p></td>
<td><p>1 行目がフィールド名、2 行目がそのデータ型の 2 行を返します。</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>返される値とその値が示すデータ型は、次のとおりです。</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><b>値</b></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>5</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>6</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>7</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>8</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>11</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>12</p></td>
</tr>
<tr class="even">
<td><p>Nextrow を指定</p></td>
<td><p>テーブルまたはクエリの現在の行の次の行のデータを返します。チャネルを開いた時点では、NextRow を指定すると最初の行のデータが返されます。現在の行が最終行のときに NextRow を指定すると、要求は失敗します。</p></td>
</tr>
<tr class="odd">
<td><p>Prevrow を指定します。</p></td>
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
<td><p>FieldCount</p></td>
<td><p>テーブルまたはクエリのフィールドの総数を返します。</p></td>
</tr>
<tr class="odd">
<td><p>SQLText</p></td>
<td><p>テーブルまたはクエリを示す SQL ステートメントです。 テーブルは、この項目はフォームで、SQL ステートメントを返します&quot;選択`*`<em>テーブル</em>です。&quot;.</p></td>
</tr>
<tr class="even">
<td><p>SQLText;<em>n</em></p></td>
<td><p><em>N</em>で、SQL ステートメントの文字のチャンクは、テーブルまたはクエリは、 <em>n</em>は最大 256 の整数を表します。 たとえば、クエリは、次の SQL ステートメントで表される: 項目&quot;SQLText; 7&quot; ] タブで区切られた次のチャンクを取得: アイテム&quot;SQLText; 7&quot; ] タブで区切られた次のチャンクを返します。</p></td>
</tr>
</tbody>
</table>


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
